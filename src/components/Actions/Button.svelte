<script>
    export let primary = false;
    export let secondary = false;
    export let accent = false;
    export let ghost = false;
    export let link = false;
    export let active = false;
    export let info = false;
    export let success = false;
    export let warning = false;
    export let error = false;
    export let outline = false;
</script>

<button
    class="btn"
    class:btn-primary={primary}
    class:btn-secondary={secondary}
    class:btn-accent={accent}
    class:btn-ghost={ghost}
    class:btn-link={link}
    class:btn-active={active}
    class:btn-info={info}
    class:btn-success={success}
    class:btn-warning={warning}
    class:btn-error={error}
    class:btn-outline={outline}
>
button
</button>