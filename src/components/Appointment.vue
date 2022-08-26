<template>
   <section class="px-5 mt-5">
      <div class="show flex justify-between items-center">
         <span class="text-blue-500 text-xs font-medium">
            My Appointment
         </span>
         <span class="text-gray-400 text-xs font-medium">
            Today
         </span>
      </div>
      
      <div class="show mt-3 bg-primary p-3 rounded-lg">
         <div class="flex justify-between">
            <div class="flex gap-2 items-start">
               <div>
                  <img src="/profile.jpg" class="rounded-lg" width="50" />
               </div>
               <div class="text-gray-100 flex flex-wrap">
                  <strong class="text-xs block w-full">Dr. Amanda Kirana</strong>
                  <p class="text-xxs">Psychologist</p>
               </div>
            </div>
            <i class="text-gray-50 text-xl fas fa-phone-square"></i>
         </div>
         <div class="bg-blue-300 mt-3 flex justify-between items-center text-gray-100 rounded-lg py-1 px-3">
            <span class="text-xxs gap-2">
               <i class="text-xxs fa fa-clock"></i>
               <small>
                  12:00 PM
               </small>
            </span>
            <span class="text-xxs">
               <i class="text-xxs mr-1 fas fa-calendar-alt"></i>
               <small>Friday, 29 September 2021</small>
            </span>
         </div>
      </div>
      
   </section>
</template>