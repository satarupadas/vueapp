<template>
  <div>
    <div class="row card list-view" v-for="user in users">
        <div class="col-xs-2 col-sm-2 col-md-2">
          <div class="wrap-image">
            <img v-bind:src="user.imagePath">
          </div>
        </div>
        <div class="col-xs-10 col-sm-10 col-md-10">
            <div class="top-info">
              <span class="full-name">{{user.firstName}} {{user.lastName}}</span>
              <span class="user-name">@{{user.userName}}</span>
              <span class="date-time">{{user.created}}</span>
            </div>
            <div class="bottom-info">
               {{user.info}}
            </div>
        </div>
    </div>
  </div>
</template>


<script>
export default {
  name: 'card',
  data(){
    return {
      title: 'Card',
      users: [
        {
          firstName: 'harri',
          lastName: 'beobide',
          userName: 'hbeobide',
          imagePath: 'logo.png',
          created: 'Tue Jul 24 15:14:48 +0000 2013',
          info: 'RT @txurtu: bene benetako zientzialariak! hhtps://t.co/olnBvvBVOD'
        },

        {
          firstName: 'garry',
          lastName: 'bolb',
          userName: 'gblob',
          imagePath: '../assets/images/image2.jpg',
          created: 'Tue oct 05 25:17:20 +0000 2013',
          info: 'RT @txurtu: bene benetako zientzialariak! hhtps://t.co/olnBvvBVOD'
        },

        {
          firstName: 'john',
          lastName: 'jacob',
          userName: 'jjacob',
          imagePath: '../assets/images/image1.jpg',
          created: 'Tue Nov 10 13:24:53 +0000 2013',
          info: 'RT @txurtu: bene benetako zientzialariak! hhtps://t.co/olnBvvBVOD'
        }
      ]


    }
  }
}
</script>
