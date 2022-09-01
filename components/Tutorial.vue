<!-- Please remove this file from your project -->
<template>
  <div class="relative flex items-top justify-center min-h-screen bg-gray-100 sm:items-center sm:pt-0">
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.1.2/dist/tailwind.min.css" rel="stylesheet">
    <div class="max-w-4xl mx-auto sm:px-6 lg:px-8">
      <a class="flex justify-center pt-8 sm:pt-0" href="https://nuxtjs.org" target="_blank">
        <svg width="218" height="45" viewBox="0 0 159 30" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M55.5017 6.81866H60.1727L70.0719 22.9912V6.81866H74.3837V29.7345H69.7446L59.8135 13.5955V29.7345H55.5017V6.81866Z" fill="#003543" /> <path d="M93.657 29.7344H89.6389V27.1747C88.7241 28.9761 86.8628 29.9904 84.5113 29.9904C80.7869 29.9904 78.3684 27.3059 78.3684 23.4423V13.2339H82.3865V22.5976C82.3865 24.8566 83.7594 26.4276 85.8171 26.4276C88.0712 26.4276 89.6389 24.6598 89.6389 22.2377V13.2339H93.657V29.7344Z" fill="#003543" /> <path d="M107.64 29.7344L103.784 24.2342L99.9291 29.7344H95.6492L101.596 21.1242L96.1074 13.2339H100.485L103.784 17.9821L107.051 13.2339H111.461L105.94 21.1242L111.886 29.7344H107.64Z" fill="#003543" /> <path d="M120.053 8.25848V13.2339H124.627V16.6063H120.053V24.7974C120.053 25.0725 120.162 25.3363 120.356 25.531C120.55 25.7257 120.813 25.8353 121.087 25.8357H124.627V29.728H121.98C118.386 29.728 116.035 27.6323 116.035 23.9687V16.6095H112.801V13.2339H114.83C115.776 13.2339 116.327 12.6692 116.327 11.7349V8.25848H120.053Z" fill="#003543" /> <path d="M134.756 24.5446V6.81866H139.066V23.1864C139.066 27.6067 136.943 29.7345 133.349 29.7345H128.332V25.8421H133.461C133.804 25.8421 134.134 25.7054 134.377 25.4621C134.619 25.2188 134.756 24.8888 134.756 24.5446Z" fill="#003543" /> <path d="M141.649 22.0409H145.799C146.029 24.6006 147.728 26.2308 150.472 26.2308C152.923 26.2308 154.623 25.2501 154.623 23.2199C154.623 18.3085 142.331 21.7129 142.331 12.9395C142.334 9.17515 145.568 6.55945 150.215 6.55945C155.05 6.55945 158.317 9.34153 158.516 13.6306H154.388C154.193 11.6341 152.632 10.2918 150.207 10.2918C147.953 10.2918 146.548 11.3397 146.548 12.9427C146.548 18.0173 159 14.2226 159 23.1576C159 27.4131 155.504 30 150.474 30C145.279 30 141.882 26.8563 141.654 22.0441" fill="#003543" /> <path d="M24.7203 29.704H41.1008C41.6211 29.7041 42.1322 29.5669 42.5828 29.3061C43.0334 29.0454 43.4075 28.6704 43.6675 28.2188C43.9275 27.7672 44.0643 27.2549 44.0641 26.7335C44.0639 26.2121 43.9266 25.6999 43.6662 25.2485L32.6655 6.15312C32.4055 5.70162 32.0315 5.32667 31.581 5.06598C31.1305 4.8053 30.6195 4.66805 30.0994 4.66805C29.5792 4.66805 29.0682 4.8053 28.6177 5.06598C28.1672 5.32667 27.7932 5.70162 27.5332 6.15312L24.7203 11.039L19.2208 1.48485C18.9606 1.03338 18.5864 0.658493 18.1358 0.397853C17.6852 0.137213 17.1741 0 16.6538 0C16.1336 0 15.6225 0.137213 15.1719 0.397853C14.7213 0.658493 14.3471 1.03338 14.0868 1.48485L0.397874 25.2485C0.137452 25.6999 0.000226653 26.2121 2.8053e-07 26.7335C-0.000226092 27.2549 0.136554 27.7672 0.396584 28.2188C0.656614 28.6704 1.03072 29.0454 1.48129 29.3061C1.93185 29.5669 2.44298 29.7041 2.96326 29.704H13.2456C17.3195 29.704 20.3239 27.9106 22.3912 24.4118L27.4102 15.7008L30.0986 11.039L38.1667 25.0422H27.4102L24.7203 29.704ZM13.0779 25.0374L5.9022 25.0358L16.6586 6.36589L22.0257 15.7008L18.4322 21.9401C17.0593 24.2103 15.4996 25.0374 13.0779 25.0374Z" fill="#00DC82" /></svg>
      </a>
      <div class="mt-8 bg-white overflow-hidden shadow sm:rounded-lg p-6">
        <h2 class="text-2xl leading-7 font-semibold">
          Search for any movie that you want
        </h2>
        <input v-model="search" class="mt-3" placeholder="Search movie">
        <button type="button" @click="click">Search</button>
      </div>

      <div class="mt-8 bg-white overflow-hidden shadow sm:rounded-lg p-6" v-for="movie of moviesMock.results">
        <p>{{ movie.original_title }} ({{ movie.release_date.split('-', 1).toString() }})</p>
        <p>Rating: {{ movie.vote_average }}</p>
        <p>Overview: {{ movie.overview }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'NuxtTutorial',
  data: () => ({
    search: '',
    movies: {},
    moviesMock: {
      'total_results': 57,
      'total_pages': 3,
      'page': 1,
      'results': [
        {
          'poster_path': '/7WsyChQLEftFiDOVTGkv3hFpyyt.jpg',
          'adult': false,
          'overview': 'As the Avengers and their allies have continued to protect the world from threats too large for any one hero to handle, a new danger has emerged from the cosmic shadows: Thanos. A despot of intergalactic infamy, his goal is to collect all six Infinity Stones, artifacts of unimaginable power, and use them to inflict his twisted will on all of reality. Everything the Avengers have fought for has led up to this moment - the fate of Earth and existence itself has never been more uncertain.',
          'release_date': '2018-04-25',
          'genre_ids': [
            12,
            28,
            878
          ],
          'id': 299536,
          'original_title': 'Avengers: Infinity War',
          'original_language': 'en',
          'title': 'Avengers: Infinity War',
          'backdrop_path': '/7WsyChQLEftFiDOVTGkv3hFpyyt.jpg',
          'popularity': 303.628,
          'vote_count': 25292,
          'video': false,
          'vote_average': 8.3
        },
        {
          'poster_path': '/or06FN3Dka5tukK1e9sl16pB3iy.jpg',
          'adult': false,
          'overview': 'After the devastating events of Avengers: Infinity War, the universe is in ruins due to the efforts of the Mad Titan, Thanos. With the help of remaining allies, the Avengers must assemble once more in order to undo Thanos\' actions and restore order to the universe once and for all, no matter what consequences may be in store.',
          'release_date': '2019-04-24',
          'genre_ids': [
            12,
            878,
            28
          ],
          'id': 299534,
          'original_title': 'Avengers: Endgame',
          'original_language': 'en',
          'title': 'Avengers: Endgame',
          'backdrop_path': '/or06FN3Dka5tukK1e9sl16pB3iy.jpg',
          'popularity': 173.113,
          'vote_count': 21674,
          'video': false,
          'vote_average': 8.3
        },
        {
          'poster_path': '/RYMX2wcKCBAr24UyPD7xwmjaTn.jpg',
          'adult': false,
          'overview': 'When an unexpected enemy emerges and threatens global safety and security, Nick Fury, director of the international peacekeeping agency known as S.H.I.E.L.D., finds himself in need of a team to pull the world back from the brink of disaster. Spanning the globe, a daring recruitment effort begins!',
          'release_date': '2012-04-25',
          'genre_ids': [
            878,
            28,
            12
          ],
          'id': 24428,
          'original_title': 'The Avengers',
          'original_language': 'en',
          'title': 'The Avengers',
          'backdrop_path': '/RYMX2wcKCBAr24UyPD7xwmjaTn.jpg',
          'popularity': 204.949,
          'vote_count': 27426,
          'video': false,
          'vote_average': 7.7
        },
        {
          'poster_path': '/4ssDuvEDkSArWEdyBl2X5EHvYKU.jpg',
          'adult': false,
          'overview': 'When Tony Stark tries to jumpstart a dormant peacekeeping program, things go awry and Earth’s Mightiest Heroes are put to the ultimate test as the fate of the planet hangs in the balance. As the villainous Ultron emerges, it is up to The Avengers to stop him from enacting his terrible plans, and soon uneasy alliances and unexpected action pave the way for an epic and unique global adventure.',
          'release_date': '2015-04-22',
          'genre_ids': [
            28,
            12,
            878
          ],
          'id': 99861,
          'original_title': 'Avengers: Age of Ultron',
          'original_language': 'en',
          'title': 'Avengers: Age of Ultron',
          'backdrop_path': '/4ssDuvEDkSArWEdyBl2X5EHvYKU.jpg',
          'popularity': 160.315,
          'vote_count': 20274,
          'video': false,
          'vote_average': 7.3
        },
        {
          'poster_path': '/8chwENebfUEJzZ7sMUA0nOgiCKk.jpg',
          'adult': false,
          'overview': 'An upcoming Phase 6 Marvel Cinematic Universe film that will conclude the Multiverse Saga.',
          'release_date': '2025-11-05',
          'genre_ids': [
            28,
            878
          ],
          'id': 1003598,
          'original_title': 'Avengers: Secret Wars',
          'original_language': 'en',
          'title': 'Avengers: Secret Wars',
          'backdrop_path': '/8chwENebfUEJzZ7sMUA0nOgiCKk.jpg',
          'popularity': 53.011,
          'vote_count': 0,
          'video': false,
          'vote_average': 0
        },
        {
          'poster_path': '/utZTb3VBrH0zR77BcISU67pHuAx.jpg',
          'adult': false,
          'overview': 'An upcoming Phase 6 Marvel Cinematic Universe film and part of The Multiverse Saga.',
          'release_date': '2025-04-30',
          'genre_ids': [
            28,
            878
          ],
          'id': 1003596,
          'original_title': 'Avengers: The Kang Dynasty',
          'original_language': 'en',
          'title': 'Avengers: The Kang Dynasty',
          'backdrop_path': '/utZTb3VBrH0zR77BcISU67pHuAx.jpg',
          'popularity': 62.861,
          'vote_count': 0,
          'video': false,
          'vote_average': 0
        },
        {
          'poster_path': '/1SbBKCbnULACOqWKN7eLfTu1gVm.jpg',
          'adult': false,
          'overview': 'When Rumpelstiltskin destroys the Magic Mirror and escapes to the modern world, the four princesses of "Once Upon a Time"-Cinderella, Sleeping Beauty, Snow White, and Rapunzel-are sucked through the portal too. Well-trained and endowed with magical powers, the four women must fight Rumpelstiltskin and his army of thralls before he enslaves everyone on Earth.',
          'release_date': '2015-03-17',
          'genre_ids': [
            28,
            14
          ],
          'id': 323660,
          'original_title': 'Avengers Grimm',
          'original_language': 'en',
          'title': 'Avengers Grimm',
          'backdrop_path': '/1SbBKCbnULACOqWKN7eLfTu1gVm.jpg',
          'popularity': 40.261,
          'vote_count': 101,
          'video': false,
          'vote_average': 4
        },
        {
          'poster_path': '/xfAcu74DRQXeM9XqFcE5MrSRzYP.jpg',
          'adult': false,
          'overview': 'When Rumpelstiltskin tries to take over Earth once and for all, The Avengers Grimm must track him down through time in order to defeat him.',
          'release_date': '2018-05-01',
          'genre_ids': [
            28,
            12,
            14
          ],
          'id': 521720,
          'original_title': 'Avengers Grimm: Time Wars',
          'original_language': 'en',
          'title': 'Avengers Grimm: Time Wars',
          'backdrop_path': '/xfAcu74DRQXeM9XqFcE5MrSRzYP.jpg',
          'popularity': 36.144,
          'vote_count': 48,
          'video': false,
          'vote_average': 4.9
        },
        {
          'poster_path': '/1p5thyQ4pCy876HpdvFARqJ62N9.jpg',
          'adult': false,
          'overview': 'British Ministry agent John Steed, under direction from "Mother", investigates a diabolical plot by arch-villain Sir August de Wynter to rule the world with his weather control machine. Steed investigates the beautiful Doctor Mrs. Emma Peel, the only suspect, but simultaneously falls for her and joins forces with her to combat Sir August.',
          'release_date': '1998-08-13',
          'genre_ids': [
            53,
            878
          ],
          'id': 9320,
          'original_title': 'The Avengers',
          'original_language': 'en',
          'title': 'The Avengers',
          'backdrop_path': '/1p5thyQ4pCy876HpdvFARqJ62N9.jpg',
          'popularity': 23.007,
          'vote_count': 582,
          'video': false,
          'vote_average': 4.4
        },
        {
          'poster_path': '/nbwvR5cfvxMtvWowIiwazVaaTVz.jpg',
          'adult': false,
          'overview': 'The children of the Avengers hone their powers and go head to head with the very enemy responsible for their parents\' demise.',
          'release_date': '2008-09-02',
          'genre_ids': [
            16,
            10751,
            28,
            12,
            878
          ],
          'id': 14613,
          'original_title': 'Next Avengers: Heroes of Tomorrow',
          'original_language': 'en',
          'title': 'Next Avengers: Heroes of Tomorrow',
          'backdrop_path': '/nbwvR5cfvxMtvWowIiwazVaaTVz.jpg',
          'popularity': 27.806,
          'vote_count': 203,
          'video': false,
          'vote_average': 6.9
        },
        {
          'poster_path': '/fKQqZEDmvKMCXEQztvMJHGou9dO.jpg',
          'adult': false,
          'overview': 'When a nuclear missile was fired at Washington in 1945, Captain America managed to detonate it in the upper atmosphere. But then he fell miles into the icy depths of the North Atlantic, where he remained lost for over sixty years. But now, with the world facing the very same evil, Captain America must rise again as our last hope for survival.',
          'release_date': '2006-02-21',
          'genre_ids': [
            28,
            16,
            10751,
            12,
            878
          ],
          'id': 14609,
          'original_title': 'Ultimate Avengers: The Movie',
          'original_language': 'en',
          'title': 'Ultimate Avengers: The Movie',
          'backdrop_path': '/fKQqZEDmvKMCXEQztvMJHGou9dO.jpg',
          'popularity': 24.387,
          'vote_count': 283,
          'video': false,
          'vote_average': 6.8
        },
        {
          'poster_path': '/h1PKqtjuTifmTU0EqM4W0Br2pHX.jpg',
          'adult': false,
          'overview': 'Mysterious Wakanda lies in the darkest heart of Africa, unknown to most of the world. An isolated land hidden behind closed borders, fiercely protected by its young king: Black Panther. But when brutal alien invaders attack, the threat leaves Black Panther with no option but to go against the sacred decrees of his people and ask for help from outsiders.',
          'release_date': '2006-08-08',
          'genre_ids': [
            12,
            16,
            28,
            878
          ],
          'id': 14611,
          'original_title': 'Ultimate Avengers 2: Rise of the Panther',
          'original_language': 'en',
          'title': 'Ultimate Avengers 2: Rise of the Panther',
          'backdrop_path': '/h1PKqtjuTifmTU0EqM4W0Br2pHX.jpg',
          'popularity': 20.844,
          'vote_count': 235,
          'video': false,
          'vote_average': 6.7
        },
        {
          'poster_path': '/ehTYWuPKwl8sXPX0I6LnvJUDaVl.jpg',
          'adult': false,
          'overview': 'When the Jade Empress steals the world\'s largest diamonds, super heroes Bikini Avenger and Thong Girl must stop her before she uses the gems to build a dangerous sci-fi weapon.',
          'release_date': '2015-02-24',
          'genre_ids': [
            35
          ],
          'id': 347158,
          'original_title': 'Bikini Avengers',
          'original_language': 'en',
          'title': 'Bikini Avengers',
          'backdrop_path': '/ehTYWuPKwl8sXPX0I6LnvJUDaVl.jpg',
          'popularity': 9.081,
          'vote_count': 15,
          'video': false,
          'vote_average': 5.5
        },
        {
          'poster_path': '/xUBZNoY7idPfqKZepnDEv7Qc8GC.jpg',
          'adult': false,
          'overview': 'The Avengers are forced to “party” with Ultron when he seeks to disassemble the team by taking control of Iron Man’s armor and enact a nefarious scheme to take over the world.',
          'release_date': '2015-11-16',
          'genre_ids': [
            10751,
            16
          ],
          'id': 368304,
          'original_title': 'LEGO Marvel Super Heroes: Avengers Reassembled!',
          'original_language': 'en',
          'title': 'LEGO Marvel Super Heroes: Avengers Reassembled!',
          'backdrop_path': '/xUBZNoY7idPfqKZepnDEv7Qc8GC.jpg',
          'popularity': 15.049,
          'vote_count': 97,
          'video': false,
          'vote_average': 6.5
        },
        {
          'poster_path': '/yymsCwKPbJIF1xcl2ih8fl7OxAa.jpg',
          'adult': false,
          'overview': 'While trying to remain a good husband and father, Superbat and the Avengers of Justice come out of retirement to stop Dark Jokester and Lisp Luthor from freezing the planet.',
          'release_date': '2018-07-20',
          'genre_ids': [
            35,
            14
          ],
          'id': 538153,
          'original_title': 'Avengers of Justice: Farce Wars',
          'original_language': 'en',
          'title': 'Avengers of Justice: Farce Wars',
          'backdrop_path': '/yymsCwKPbJIF1xcl2ih8fl7OxAa.jpg',
          'popularity': 14.855,
          'vote_count': 11,
          'video': false,
          'vote_average': 3.8
        },
        {
          'poster_path': '/coS6rIaucxDzq20kiJozTgQ0Nmk.jpg',
          'adult': false,
          'overview': 'Witness Marvel\'s epic journey, from its comic book origins to its blockbuster film franchises, through seven exclusive featurettes. Get the inside story, with exclusive behind-the-scenes footage and cast interviews, and discover the history behind its legendary characters and films -- Iron Man, The Incredible Hulk, Iron Man 2, Thor, Captain America: The First Avenger, and Marvel\'s The Avengers! With over 90 minutes of original footage, this is your all-access pass to Marvel and Phase One of the Marvel Cinematic Universe!',
          'release_date': '2012-09-25',
          'genre_ids': [
            99
          ],
          'id': 448366,
          'original_title': 'Building the Dream: Assembling the Avengers',
          'original_language': 'en',
          'title': 'Building the Dream: Assembling the Avengers',
          'backdrop_path': '/coS6rIaucxDzq20kiJozTgQ0Nmk.jpg',
          'popularity': 9.899,
          'vote_count': 23,
          'video': true,
          'vote_average': 8.3
        },
        {
          'poster_path': '/2kBT7KONKQTIhkMc2ZtPU11E8Ky.jpg',
          'adult': false,
          'overview': 'Joss Whedon and others in interviews discussing the aims for this new franchise.',
          'release_date': '2012-09-25',
          'genre_ids': [],
          'id': 448368,
          'original_title': 'The Avengers: A Visual Journey',
          'original_language': 'en',
          'title': 'The Avengers: A Visual Journey',
          'backdrop_path': '/2kBT7KONKQTIhkMc2ZtPU11E8Ky.jpg',
          'popularity': 9.374,
          'vote_count': 13,
          'video': true,
          'vote_average': 7.7
        },
        {
          'poster_path': '/mEd93PE41k5bmPEbsBytOn1REti.jpg',
          'adult': false,
          'overview': 'A recreation of ‘Avengers: Infinity War’s dark ending using Lego bricks.',
          'release_date': '2018-05-17',
          'genre_ids': [],
          'id': 1009770,
          'original_title': 'Avengers Infinity War: The End',
          'original_language': 'en',
          'title': 'Avengers Infinity War: The End',
          'backdrop_path': '/mEd93PE41k5bmPEbsBytOn1REti.jpg',
          'popularity': 8.524,
          'vote_count': 2,
          'video': false,
          'vote_average': 3
        },
        {
          'poster_path': '/Akd3Aqrr2q8PLKOCPOkOnB3AoJk.jpg',
          'adult': false,
          'overview': 'Charlie and Rhonda are a sweet and comfortable married couple on vacation with their lovely daughter Daphne. They find a rundown boarding house and its haggard owner, Joseph, an ex-con whose mother has just died and left him the house. He doesn\'t know why this cheerful couple would want to vacation in the worst part of Los Angeles, but he doesn\'t know they\'re vacationing from outer space, and their idea of fun is murdering lowlife out on the streets',
          'release_date': '1996-08-03',
          'genre_ids': [
            35,
            878
          ],
          'id': 58906,
          'original_title': 'Alien Avengers',
          'original_language': 'en',
          'title': 'Alien Avengers',
          'backdrop_path': '/Akd3Aqrr2q8PLKOCPOkOnB3AoJk.jpg',
          'popularity': 1.81,
          'vote_count': 5,
          'video': false,
          'vote_average': 6
        },
        {
          'poster_path': '/7nA9AjJ8iZvbBPsFPC2FNoFj568.jpg',
          'adult': false,
          'overview': 'When Thanos steals the quantum tunnel, the Avengers embark on a mission to stop him from changing history.',
          'release_date': '2022-01-17',
          'genre_ids': [
            10751,
            16,
            28,
            12
          ],
          'id': 940543,
          'original_title': 'LEGO Marvel Avengers: Time Twisted',
          'original_language': 'en',
          'title': 'LEGO Marvel Avengers: Time Twisted',
          'backdrop_path': '/7nA9AjJ8iZvbBPsFPC2FNoFj568.jpg',
          'popularity': 3.082,
          'vote_count': 2,
          'video': false,
          'vote_average': 5
        }
      ]
    }
  }),
  methods: {
    click () {
      if (this.search.length > 2){
        console.log('click', this.search)
        // this.fetchMovies()
      }
    },
    async fetchMovies () {
      const token = 'NWY1NmY0MzYtNmY2OS00ZDFhLWEwOWYtNzNlNzczYzZiM2Ey'
      const config = {
        headers: { Authorization: `Bearer ${token}` }
      }
      const bodyParameters = {
        'query': 'avengers'
      }
      this.movies = await this.$axios.$post(
        'https://api.m3o.com/v1/movie/Search',
        bodyParameters,
        config
      ).then(resp => {
        return resp
      }).catch(console.log)
    }
  }
}
</script>
