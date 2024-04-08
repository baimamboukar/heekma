<script setup lang="ts">
import {
  LayoutDashboard,
  DatabaseZap,
  PlugZap2,
  Users,
  LineChart,
  Settings,
} from "lucide-vue-next";

const items = [
  {
    icon: LayoutDashboard,
    title: "Dashboard",
    href: "/",
  },
  {
    icon: DatabaseZap,
    title: "Data Sources",
    href: "/sources",
    badge: 6,
  },
  {
    icon: PlugZap2,
    title: "Integrations",
    href: "/integrations",
  },
  {
    icon: Users,
    title: "Manage Users",
    href: "/authorization",
  },
  {
    icon: LineChart,
    title: "Analytics",
    href: "/dashboard/analytics",
  },
  {
    icon: Settings,
    title: "Settings",
    href: "/settings",
  },
];
</script>

<template>
  <div class="flex-1">
    <nav class="grid items-start px-2 text-sm font-medium lg:px-4">
      <div v-for="item in items">
        <a
          :key="item.href"
          :href="item.href"
          class="flex items-center gap-3 rounded-lg px-3 py-2 text-muted-foreground transition-all hover:text-primary"
        >
          <component :is="item.icon" class="h-4 w-4" />
          {{ item.title }}
          <Badge
            v-if="item.badge"
            class="ml-auto flex h-6 w-6 shrink-0 items-center justify-center rounded-full"
          >
            {{ item.badge }}
          </Badge>
        </a>
      </div>
    </nav>
  </div>
</template>
