<!--
Copyright: Ankitects Pty Ltd and contributors
License: GNU AGPL, version 3 or later; http://www.gnu.org/licenses/agpl.html
-->
<script>
    import Col from "$lib/components/Col.svelte";
    import ConfigInput from "$lib/components/ConfigInput.svelte";
    import Row from "$lib/components/Row.svelte";

    export let date;
    $: date = date ? date : "1970-01-01";
</script>

<div>
    <ConfigInput>
        <Row --cols={2}>
            <Col>
                <slot />
            </Col>
            <Col>
                <input bind:value={date} type="date" />
            </Col>
        </Row>
    </ConfigInput>
</div>

<style>
    input {
        width: 100%;
        -webkit-appearance: none;
        appearance: none;
        height: 1.5em;
    }
</style>
