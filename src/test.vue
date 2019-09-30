<template>
<div>
    <p>sadasdasdasdasdasd</p>
    <div class="modal">
        <ustModal>
            <h3 slot="title">Custom Header</h3>
            <div slot="body">
                <p>This is a test</p>
                <p>This is a test</p>
                <p>This is a test</p>
                <p>This is a test</p>
                <p>This is a test</p>
            </div>
            <div slot="actions">
                <button @click="model=false">Cancel</button>
                <button @click="$emit('close')">OK</button>
            </div>
        </ustModal>
    </div>
</div>
</template>

<script>
import ustModal from './ustModal'
export default {
    components: {
        ustModal
    },
    data: {
        modal: true
    }
}
</script>

<style scoped>
.modal{
    font-size: 16px;
text-rendering: optimizeLegibility;
-webkit-font-smoothing: antialiased;
-webkit-tap-highlight-color: rgba(0, 0, 0, 0);
font-family: "Roboto", sans-serif;
line-height: 1.5;
color: rgba(0, 0, 0, 0.87);
box-sizing: inherit;
background-repeat: no-repeat;
padding: 0;
margin: 0;
align-items: center;
display: flex;
height: 100%;
justify-content: center;
left: 0;
pointer-events: none;
position: fixed;
top: 0;
transition: 0.2s cubic-bezier(0.25, 0.8, 0.25, 1), z-index 1ms;
width: 100%;
outline: none;
z-index: 202;
}
</style>