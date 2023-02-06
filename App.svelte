
<script>
    import {onMount} from "svelte"
    import {MindmapComponent, InspectorComponent} from "@jsplumb-components/mindmap-svelte"

    let mindmapBuilder

    onMount(async () => {
        mindmapBuilder.loadUrl("./mindmap-1.json", () => {
            mindmapBuilder.zoomToFit()
        })
    })

</script>


<div id="canvas">
    <MindmapComponent id="myMindmap" bind:this={mindmapBuilder}/>
</div>

<div id="rhs">
    <InspectorComponent mindmapId="myMindmap"></InspectorComponent>
</div>

