<template>
  <ul
    class="c-contentList"
    :class="contentListStyle"
  >
    <li class="c-contentList_list">
      <a href="/">home</a>
    </li>
    <li class="c-contentList_list">
      <a href="#">page</a>
    </li>
    <li class="c-contentList_list">
      <a href="#">page</a>
    </li>
    <li class="c-contentList_list">
      <a href="#">page</a>
    </li>
    <li class="c-contentList_list">
      <a href="#">page</a>
    </li>
  </ul>
</template>

<script>
export default {
  props: {
    contentListStyle: {
      type: String,
    }
  },
}
</script>