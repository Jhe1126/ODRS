<script setup>
import BreezeApplicationLogo from '@/Components/ApplicationLogo.vue';
import { Link } from '@inertiajs/inertia-vue3';
</script>

<template>

    <div class="min-h-screen flex flex-col sm:justify-center items-end pt-6 sm:pt-0 bg-green-100 grid grid-cols-2 gap-4 place-content-around h-48 ... ">
        
        <div>
            <p class="text-white text-5xl flex justify-start flex indent-56"><b>MMSU</b></p>
            <p class="text-white text-5xl flex justify-start flex indent-28"><b>Registrar Online Document</b></p>
            <p class="text-white text-5xl flex justify-center"><b>Request System</b></p>
            <br><br><br><br><br><br><br><br>
            <p class="text-white text-3xl flex justify-start">
                <b class="indent-10">Is this your first time here?</b>
            </p>
            <br>
            <h1 class="text-white text-1xl flex justify-start indent-10">For<b>Students:</b></h1>
            <h1 class="text-white text-1xl flex justify-start indent-10">To proceed,use<p class="underline underline-offset-1 ...">Student Portal </p>credentials (Student</h1>
            <h1 class="text-white text-1xl flex justify-start items-start">&emsp;&emsp;&emsp;&ensp;&nbsp;number and Password).</h1>
            <br>
            <h1 class="text-white text-1xl flex justify-start items-start">&emsp;&emsp;&emsp;&ensp;&nbsp;For&nbsp;<b> Faculty:</b></h1>
            <h1 class="text-white text-1xl flex justify-start items-start">&emsp;&emsp;&emsp;&ensp;&nbsp;Request for an authentication credential from ITC.</h1>
            <br><br><br><br><br><br><br><br>
            <p class="text-white text-lg">&emsp;&emsp;&emsp;please email us at <u>itc-support@mmsu.edu.ph</u>
            <br>&emsp;&emsp;&emsp;with the subject "Student Portal - Password Reset"<br>
            &emsp;&emsp;&emsp;and attacha copy of your University ID. If you do not
            <br>&emsp;&emsp;&emsp;have your University ID yet, please email us
            <br>&emsp;&emsp;&emsp;your fullname, student number and degree.</p>
            
        </div>
        

        <div class="sm:max-w-md mt-6 px-6 py-4 overflow-hidden sm:rounded-lg">
            <slot />
        </div>
    </div>
    
</template>
