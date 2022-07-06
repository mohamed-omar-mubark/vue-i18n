<template>
  <p>{{ $t("content") }}</p>
</template>

<script>

export default ({
  name: "HelloI18n",
});
</script>

<i18n>
{
  "en": {
    "content": "English Content."
  },
  "fr": {
    "content": "Contenu en français."
  },
  "ar": {
    "content": "المحتوى باللغة العربية."
  }
}
</i18n>
