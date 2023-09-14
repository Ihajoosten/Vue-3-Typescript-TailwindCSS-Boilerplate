<template>
  <div class="pt-0.5">
    <!-- App header -->
    <AppHeader />

    <!-- Render active component contents with vue transition -->
    <router-view v-slot="{ Component }">
      <transition name="fade" mode="out-in">
        <component :is="Component" />
      </transition>
    </router-view>

    <!-- App footer -->
    <AppFooter />
  </div>
</template>

<script lang="ts">
import feather from "feather-icons";
import AppHeader from "@/components/shared/AppHeader.vue";
import AppFooter from "@/components/shared/AppFooter.vue";

export default {
  components: {
    AppHeader,
    AppFooter,
  },
  data: () => {
    return {};
  },
  mounted() {
    feather.replace();
  },
  updated() {
    feather.replace();
  },
};
</script>

<style scoped>
.fade-enter-active {
  animation: coming 0.4s;
  animation-delay: 0.2s;
  opacity: 0;
}

.fade-leave-active {
  animation: going 0.4s;
}

@keyframes going {
  from {
    transform: translateX(0);
  }
  to {
    transform: translateX(-30px);
    opacity: 0;
  }
}
@keyframes coming {
  from {
    transform: translateX(-30px);
    opacity: 0;
  }
  to {
    transform: translateX(0px);
    opacity: 1;
  }
}
</style>
