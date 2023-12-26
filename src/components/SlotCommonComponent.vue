<template>
    <div class="card w-50 mx-auto">
        <div class="card-header">
            <!-- Default header is empty if parent component do not provide -->
            <slot name="header"></slot>
        </div>

        <div class="card-body py-3">
            <!-- This is default slots that contain slot unsign  -->
            <slot></slot>
        </div>

        <div class="card-footer">
            <!-- Default footer is empty if parent component do not provide -->
            <slot name="footer"></slot>
        </div>
    </div>
</template>

<script>
export default {}
</script>
