<script setup>
import BreezeButton from '@/Components/Button.vue';
import BreezeCheckbox from '@/Components/Checkbox.vue';
import BreezeGuestLayout from '@/Layouts/Guest.vue';
import BreezeInput from '@/Components/Input.vue';
import BreezeLabel from '@/Components/Label.vue';
import BreezeValidationErrors from '@/Components/ValidationErrors.vue';
import { Head, Link, useForm } from '@inertiajs/inertia-vue3';

defineProps({
    canResetPassword: Boolean,
    status: String,
});

const form = useForm({
    email: '',
    password: '',
    remember: false
});

const submit = () => {
    form.post(route('login'), {
        onFinish: () => form.reset('password'),
    });
};
</script>

    
<template >
    <body>
    <BreezeGuestLayout class="bg-auto bg-no-repeat bg-center ..." style="background-image: url('images/background.png');">
        
        <Head title="Log in" />
    
        <BreezeValidationErrors class="mb-4" />
        
        <div v-if="status" class="mb-4 font-medium text-sm text-green-600">
            {{ status }}
        </div>
        
        <form @submit.prevent="submit">
            <div>
            <img class="object-contain h-48 w-96 ..." src="images/logo.png" alt="" >
            </div>
            <br><br>
            <div class="text-center ...">
                <h1 class="text-3xl ..."><b>Login</b></h1>
            </div>
            <br><br>
            <div>
                <BreezeLabel for="email" />
                <BreezeInput id="email" placeholder="Student Number" type="text" class="mt-1 block w-full" v-model="form.email" required autofocus autocomplete="username" />
            </div>

            <div class="mt-4">
                <BreezeLabel for="password" />
                <BreezeInput id="password" placeholder="Password" type="password" class="mt-1 block w-full" v-model="form.password" required autocomplete="current-password" />
            </div>

            <div class="block mt-4">
                <label class="flex items-center">
                    <BreezeCheckbox name="remember" v-model:checked="form.remember" />
                    <span class="ml-2 text-sm text-gray-600">Remember me</span>
                </label>
            </div>
               <div class="flex justify-center">
                <BreezeButton class="ml-4 flex" :class="{ 'opacity-25': form.processing }" :disabled="form.processing">
                    Log in
                </BreezeButton>
            </div>
            <div class="flex justify-start">
                <Link v-if="canResetPassword" :href="route('password.request')" class="underline text-sm text-gray-600 hover:text-gray-900">
                    Forgot your password?
                </Link>
               </div> 
               <div>
                <br><br><br><br><br><br><br><br>
               </div>
        </form>

    </BreezeGuestLayout>

</body>
</template>
