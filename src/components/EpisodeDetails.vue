<template lang="html">
    <div v-if='episode'>
        <h2>Episode Details:</h2>
        <span>{{ episode.title }}</span>
        <ul>
            <li>Original US airdate:</li>
            <li>- {{ episode.usAirDate }}</li>
            <br>
            <li>In-universe events:
            <li v-if="episode.stardateFrom !== null">
                - Stardate {{ episode.stardateFrom }} to Stardate:{{ episode.stardateTo }}
            </li>
            <p></p>
            <br>
            <li>
                <a href="https://memory-alpha.fandom.com/wiki/Portal:Main">Read more at Memory Alpha</a>
            </li>
            <br>
            <li>
                <a href="https://memory-beta.fandom.com/wiki/Main_Page">Read even more at Memory Beta</a>
            </li>
            <br>
        </ul>
    </div>
</template>

<script>
import AllSeasonsList from './AllSeasonsList';
import AllEpisodesList from './AllEpisodesList';
import AllEpisodesListItem from './AllEpisodesListItem';


export default {
    name: 'episode-details',
    props: ['episode'],


components: {
    "all-seasons-list": AllSeasonsList,
    "all-episodes-list": AllEpisodesList,
    "all-episodes-list-item": AllEpisodesListItem
}
}
</script>

<style lang="css" scoped>

ul {
    list-style: none;
}

</style>