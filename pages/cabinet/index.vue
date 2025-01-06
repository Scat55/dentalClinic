<script setup lang="ts">
import { Skeleton } from '@/components/ui/skeleton'
</script>

<template>
  <div class="grid w-full gap-4">
    <header class="flex items-start justify-between">
      <div class="grow">
        <p>Вся информация о ваших клиентах !</p>
        <h1>Личный кабинет</h1>
      </div>
      <Skeleton class="w-[120px] h-[36px]" />
    </header>
    <main class="grid gap-4">
      <div class="flex items-center gap-4">
        <Skeleton v-for="(item, index) in 3" :key="index" class="w-full rounded-2 xl h-[260px]" />
        <!--        Здесь будут Tabs с 1) Сколько записей на сегодня-->
        <!--        2) Записи на эту неделю-->
        <!--        3) Записи на этот месяц-->
      </div>
      <section>
        <Skeleton class="w-full h-[600px] bg-neutral-200 rounded-2xl" />
        <!--        Здесь будет статистика клиентов за текущий месяц Chart-->
      </section>
    </main>
  </div>
</template>
