<template>
<div>
    <div class="modal">
        <button @click="modal = true">Open</button>
        <button @click="modal = false">close</button>
        <ustModal v-model.sync="modal"> 
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
    data: () =>  ({
        modal: true,
    }),
    methods: {
        input(data){
            this.modal = data
        }
    }
}
</script>
