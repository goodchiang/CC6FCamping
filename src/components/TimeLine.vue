<template>
   <li class="timeline-event" data-aos="fade-up">
        <label class="timeline-event-icon"></label>
        <div class="timeline-event-copy">
            <p class="timeline-event-thumbnail">{{ time }}</p>
            <h4>eines Web-Studios</h4>
            <h3>{{ campSite }}</h3>
        </div>
    </li>
</template>

<script>
export default {
    props: ["time", "campSite"]
}
</script>

<style>

</style>