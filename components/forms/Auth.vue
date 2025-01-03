<!--TODO: Сделать валидацию-->
<script setup lang="ts">
import { Button } from '@/components/ui/button'
import { Card, CardContent, CardDescription, CardFooter, CardHeader, CardTitle } from '@/components/ui/card'
import { Input } from '@/components/ui/input'
import { Label } from '@/components/ui/label'

</script>

<template>
  <Card class="w-full max-w-sm">
    <CardHeader>
      <CardTitle class="text-2xl">
        Вход
      </CardTitle>
      <CardDescription />
    </CardHeader>
    <CardContent class="grid gap-4">
      <div class="grid gap-2">
        <Label for="login">Логин</Label>
        <Input id="login" type="text" placeholder="Введите логин" required />
      </div>
      <div class="grid gap-2">
        <Label for="password">Пароль</Label>
        <Input id="password" type="password" required />
      </div>
    </CardContent>
    <CardFooter>
      <Button class="w-full">
        Войти
      </Button>
    </CardFooter>
  </Card>
</template>
