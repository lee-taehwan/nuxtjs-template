<template>
  <CommonHeader v-if="!disableHeaderRouteNames.includes(route.name)" />
  <div>error page</div>
  <CommonFooter v-if="!disableFooterRouteNames.includes(route.name)" />
</template>

<script setup>
const route = useRoute();
const disableHeaderRouteNames = useState(() => []);
const disableFooterRouteNames = useState(() => []);

const { error } = defineProps({
  error: Object,
});
</script>
