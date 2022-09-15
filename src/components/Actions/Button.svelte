<script>
    export let label = ''
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
    export let lg = false;
    export let md = false;
    export let sm = false;
    export let xs = false;
    export let wide = false;
    export let block = false;
    export let glass = false;
    export let loading = false;
    export let disabled = false;
    export let square = false;
    export let circle = false;
    export let noAnimate= false;
    export let bp = {
        sm:'',
        md:'',
        lg:''
    }

    $: hasBp = Object.values(bp).filter(val => !!val).length > 0 ? true : false;

</script>

<button
    class="btn {hasBp ? `sm:btn-${bp.sm} md:btn-${bp.md} lg:btn-${bp.lg}`: ''}"
    class:btn-wide={wide}
    class:btn-block={block}
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
    class:btn-lg={!hasBp && lg}
    class:btn-sm={!hasBp && sm}
    class:btn-md={!hasBp && md}
    class:btn-xs={!hasBp && xs}
    class:glass={glass}
    class:loading={loading}
    class:btn-square={square}
    class:btn-circle={circle}
    class:no-animation={noAnimate}
    {disabled}
>
{#if !square && !circle}
    <slot name="start"></slot>
        {#if !label}
            <slot></slot>
        {:else}
            {label}
        {/if}
    <slot name="end"></slot>
    {:else}
    <slot></slot>
{/if}
</button>