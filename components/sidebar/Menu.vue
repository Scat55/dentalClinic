<script setup lang="ts">
import type SidebarMenu from '~/types/sidebar-menu'

const items = ref<SidebarMenu[]>([
  { title: 'Записи', link: ' cabinet/records', icon: 'vaadin:records' },
  { title: 'Продажи', link: 'cabinet/sales', icon: 'carbon:sales-ops' },
  { title: 'Финансы', link: 'cabinet/finance', icon: 'material-symbols:finance-mode-rounded' },
  { title: 'Склад', link: 'cabinet/warehouse', icon: 'prime:warehouse' },
  { title: 'Клиенты', link: 'cabinet/clients', icon: 'weui:contacts-outlined' },
  { title: 'Аналитика', link: 'cabinet/analytics', icon: 'clarity:analytics-line' }
])
</script>

<template>
  <div>
    <header class="flex items-center gap-2 p-4 hover:scale-[101%] transition cursor-pointer">
      <Logo class="text-blue-700" />
      <p class="font-bold lg:text-xl ">
        Клиника <span class="text-blue-700">Доверие</span>
      </p>
    </header>
    <div class="px-4 grow">
      <div class="grid gap-4">
        <div
          v-for="item in items"
          :key="item.title"
          class="flex items-center
          gap-2 px-2 py-1 transition
          rounded cursor-pointer hover:bg-neutral-100"
        >
          <Icon size="20" :name="item.icon" color="black" />
          <span>{{ item.title }}</span>
        </div>
      </div>
    </div>
  </div>
</template>
