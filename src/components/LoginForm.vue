<template>
  <div class="message">
    <h1>{{ msg }}</h1>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
class LoginForm extends Vue {
  @Prop() private msg!: string;
}

export default LoginForm;
</script>
