
<template>
  <GuestLayout title="Сбросить пароль">
      <form class="space-y-6" action="#" method="POST">
        <div>
            <div class="flex items-center justify-between">
              <label for="new-password" class="block text-sm font-medium leading-6 text-gray-900">Новый пароль</label>
              
            </div>
            <div class="mt-2">
              <input id="new-password" name="new-password" type="password" autocomplete="current-password"  class=" block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6" />
            </div>
          </div>
          <div>
            <div class="flex items-center justify-between">
              <label for="password-repeat" class="block text-sm font-medium leading-6 text-gray-900">Повторить пароль</label>
              
            </div>
            <div class="mt-2">
              <input id="password-repeat" name="password-repeat" type="password" autocomplete="current-password"  class=" block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6" />
            </div>
          </div>
        

        <div>
          <button type="submit"
            class="flex w-full justify-center rounded-md bg-indigo-600 px-3 py-1.5 text-sm font-semibold leading-6 text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600">Сбросить</button>
        </div>
      </form>
      <p class="mt-10 text-center text-sm text-gray-500">
          
          {{ ' ' }}
          <router-link :to="{name: 'login'}" class="font-semibold leading-6 text-indigo-600 hover:text-indigo-500">Вернуться к аутентификации</router-link>
        </p>
      </GuestLayout>
</template>
  
<script setup>
import GuestLayout from "../components/GuestLayout.vue";
</script>
