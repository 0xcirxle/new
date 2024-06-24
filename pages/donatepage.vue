<template>
  <div class="flex flex-col flex-grow items-center justify-center mt-10">
    <div class="max-w-96 min-h-96 mx-auto border-2 border-black rounded-lg">
      <h1 class="p-5">gm lorem ipsum!</h1>
      <p class="p-5 pt-2">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam auctor, nunc id aliquam tincidunt, nisi velit ultricies nunc, nec tincidunt nunc nunc vel nunc.</p>
      <UDropdown class="p-5 min-w-80" :items="items" :popper="{ placement: 'bottom-start' }">
        <UButton class="min-w-80" color="white" label="Options" trailing-icon="i-heroicons-chevron-down-20-solid" />
      </UDropdown>
    </div>
  </div>
</template>

<script setup lang="ts">
  const items = [
    [{
      label: 'Profile',
    }], [{
      label: 'Edit',
    }]
  ]
</script>