<template>
    <div class="page page--header">
        <CoreSection
            :order="instances++"
        >
            <HeroBannerFace />
        </CoreSection>
        <CoreSection
            :order="instances++"
            :title="$t('section.lastPosts')"
        >
            <PostVerticalList>
                <PostResume 
                    v-for="(post, i) in [1,2,3,4,5,6]"
                    :key="i"
                    :index="i" 
                />
            </PostVerticalList>
        </CoreSection>
    </div>
</template>

<script>
    import CoreSection from '@/components/Core/Section.vue'
    import HeroBannerFace from '@/components/Banner/HeroFace.vue'
    import PostResume from '@/components/Cards/Post/Resume.vue'
    import PostVerticalList from '@/components/Cards/Post/VerticalList.vue'

    export default {
        components: {
            HeroBannerFace,
            CoreSection,
            PostResume,
            PostVerticalList
        },
        setup() {
            const instances = 0
            return {
                instances
            }
        }
      
    }
</script>

<style lang="postcss">

</style>