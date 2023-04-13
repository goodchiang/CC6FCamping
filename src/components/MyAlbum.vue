<template>
    <div class="col-md-4 col-sm-6 graphics ads">
        <a id="demo07" href="#animatedModal" class="portfolio_item">
            <img :src="snapshot" alt="image" class="img-responsive" />
            <div class="portfolio_item_hover">
                <div class="portfolio-border clearfix">
                    <div class="item_info"> 
                        <span>{{ campSite }}</span> 
                        <em>Graphics / Ads</em>
                    </div>
                </div>
            </div>
        </a>
    </div>
</template>

<script>
export default {
    props:["snapshot", "campSite"]
}
</script>

<style>

</style>