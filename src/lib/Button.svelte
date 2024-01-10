<script>
    export let title = "Default";
    export let size = "small";
    export let shadow = true;
</script>

<button class={size === "small" ? "size-sm" : "size-lg"} class:shadow>
    <slot>{title}</slot>
</button>

<style lang="scss">
  button {
    display: block;
    border: none;
    background-color: #ff3e00;
    transition: background-color 3s ease;
    color: #ffffff;
    font-weight: bold;
    border-radius: 5px;
    cursor: pointer;
    min-width: 120px;

    &:hover {
      background-color: rgba(0, 0, 0, 0.4), #ff3e00;
    }

    &.size-sm {
      padding: 15px 20px;
    }

    &.size-lg {
      padding: 20px 25px;
      font-size: 1.125rem;
    }

    &.shadow {
      box-shadow: 0 0 10px rgba(40, 1, 1, 0.57);
    }
  }
</style>