<script>
    import PageWrapper from "@/components/base/PageWrapper.svelte";

    export let nobranding = false;
</script>

<PageWrapper class="full-page" center>
    <div class="wrapper wrapper-sm m-b-xl panel-wrapper">
        {#if !nobranding}
            <div class="block m-b-base">
                <figure class="logo">
                    <img
                        src="{import.meta.env.BASE_URL}images/logo.svg"
                        alt="Upswing Backend"
                        width="55"
                    />
                    <span class="txt">Upswing <strong>Backend</strong></span>
                </figure>
            </div>
            <div class="clearfix" />
        {/if}

        <slot />
    </div>
</PageWrapper>

<style>
    .panel-wrapper {
        animation: slideIn 200ms;
    }
</style>
