<template>
<div>
    <div class="modal">
        <button @click="modal = true">Open</button>
        <!-- <button @click="modal = false">close</button> -->
        <ustModal v-model="modal" :styles="styles"> 
            <h3 slot="title">Custom Header</h3>
            <div slot="body">
                <p>This Modal Body</p>
                <p>This Modal Body</p>
                <p>This Modal Body</p>
                <p>This Modal Body</p>
                <p>This Modal Body</p>
            </div>
            <div slot="actions">
                <button @click="modal=false">Cancel</button>
                <button @click="modal=false">OK</button>
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
    data: () =>  ({
        modal: true,
        styles: {
            width: "500px"
        }
    })
}
</script>
