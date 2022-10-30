<template>
  <section id="home">
    <div class="hooper">
      <div class="action">
        <h1>Hoşniýetli hyzmatdaşlyk merkezi.</h1>
        <button class="anket">{{$tt('Anketa tabşyrmak','Отправить анкету')}}</button>
      </div>
      <hooper :settings="hooperSettings">
        <slide>
          <div class="slider1"></div>
        </slide>
        <slide>
          <div class="slider1 slider2"></div>
        </slide>
        <slide>
          <div class="slider1 slider3"></div>
        </slide>
        <slide>
          <div class="slider1 slider4"></div>
        </slide>
        <hooper-navigation slot="hooper-addons"></hooper-navigation>
        <hooper-pagination slot="hooper-addons"></hooper-pagination>
        <hooper-progress slot="hooper-addons"></hooper-progress>
      </hooper>
    </div>
    <section id="about">
      <div class="left">
        <h1>{{$tt('Siyahatçylyk','Туризм')}}</h1>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ipsa
          dignissimos, vitae similique rem blanditiis sapiente beatae doloremque
          quod non illo! Odit sit itaque iure assumenda libero, dolor facere
          aspernatur rerum incidunt facilis sequi ut nobis dicta nam aliquam id
          natus minima nesciunt quo vel! Voluptate, quidem eveniet. Obcaecati,
          vitae labore in asperiores nisi ut odit eum nesciunt tempore pariatur
          sunt deleniti illo qui ratione numquam laboriosam soluta illum
          excepturi voluptas ducimus cumque aliquam. Cumque deleniti quaerat
          ducimus aliquid doloribus quidem obcaecati laudantium corrupti soluta
          voluptatibus architecto accusantium maxime enim dolorem necessitatibus
          repellat modi, culpa sapiente suscipit dolorum. Et, deleniti corporis!
        </p>
      </div>
      <div class="right">
        <div class="right_top">
          <h1>{{$tt('Distribyutor','Дистрибьютор')}}</h1>
          <img src="./../assets/image/marka-titiz-1 2.svg" alt="" />
        </div>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ipsa
          dignissimos, vitae similique rem blanditiis sapiente beatae doloremque
          quod non illo! Odit sit itaque iure assumenda libero, dolor facere
          aspernatur rerum incidunt facilis sequi ut nobis dicta nam aliquam id
          natus minima nesciunt quo vel! Voluptate, quidem eveniet. Obcaecati,
          vitae labore in asperiores nisi ut odit eum nesciunt tempore pariatur
          sunt deleniti illo qui ratione numquam laboriosam soluta illum
          excepturi voluptas ducimus cumque aliquam. Cumque deleniti quaerat
          ducimus aliquid doloribus quidem obcaecati laudantium corrupti soluta
          voluptatibus architecto accusantium maxime enim dolorem necessitatibus
          repellat modi, culpa sapiente suscipit dolorum. Et, deleniti corporis!
        </p>
      </div>
    </section>
    <section id="services">
      <div class="title">
        <h1>{{$tt('Turlar','Туры')}}</h1>
      </div>
      <div class="cards_top">
     <div class="card_middle">
      <Card
        v-for="(e, i) in tur"
        :key="i"
        :info="e"
      />
     </div>
      </div>
    </section>
    <section id="contact">
      <div class="content">
        <h1>{{$tt('Habarlaşmak','Cвязаться с нами')}}</h1>
        <div class="left">
          <div class="left_input">
            <label for="text">{{$tt('Adynyz','Имя')}}</label>
            <input
              type="text"
              class="text"
              placeholder="Adynyz"
              pattern=""
              required
            />
            <label for="email">{{$tt('Email','Электронная почта')}}</label>
            <input type="email" class="email" placeholder="Email" required />
            <label for="coment">{{$tt('Hatynyz','Письмо')}}</label>
            <textarea
              name="coment"
              id="coment"
              cols="30"
              rows="10"
              placeholder="Hatynyz"
            ></textarea>
            <button class="btn">{{$tt('Ugradyň','Отправить')}}</button>
          </div>
          <div class="right_contact">
            <h1>{{$tt('Habarlaşmak üçin:','Cвязаться с нами:')}}</h1>
            <p>
              <svg
                width="25"
                height="25"
                viewBox="0 0 25 25"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M15.6769 5.20833C16.6943 5.40684 17.6294 5.90443 18.3624 6.63743C19.0954 7.37043 19.593 8.30548 19.7915 9.32291M15.6769 1.04166C17.7907 1.27649 19.7619 2.2231 21.2667 3.72605C22.7716 5.229 23.7207 7.19897 23.9582 9.3125M22.9165 17.625V20.75C22.9177 21.0401 22.8582 21.3273 22.742 21.5931C22.6258 21.8589 22.4554 22.0975 22.2416 22.2936C22.0278 22.4897 21.7754 22.639 21.5006 22.732C21.2258 22.8249 20.9346 22.8594 20.6457 22.8333C17.4403 22.485 14.3613 21.3897 11.6561 19.6354C9.13923 18.0361 7.00539 15.9023 5.40608 13.3854C3.64564 10.6679 2.55008 7.57395 2.20816 4.35416C2.18213 4.06611 2.21636 3.77579 2.30868 3.50169C2.401 3.22759 2.54938 2.97572 2.74438 2.7621C2.93937 2.54849 3.17671 2.37782 3.44128 2.26096C3.70585 2.1441 3.99185 2.0836 4.28108 2.08333H7.40608C7.91161 2.07836 8.4017 2.25737 8.785 2.58701C9.1683 2.91665 9.41866 3.37442 9.48941 3.875C9.62131 4.87507 9.86592 5.857 10.2186 6.80208C10.3587 7.17492 10.3891 7.58012 10.306 7.96966C10.2229 8.35921 10.0299 8.71678 9.74983 9L8.42691 10.3229C9.90978 12.9308 12.0691 15.09 14.6769 16.5729L15.9998 15.25C16.283 14.9699 16.6406 14.7769 17.0302 14.6938C17.4197 14.6108 17.8249 14.6411 18.1977 14.7812C19.1428 15.1339 20.1248 15.3785 21.1248 15.5104C21.6308 15.5818 22.093 15.8367 22.4233 16.2266C22.7536 16.6164 22.9292 17.1141 22.9165 17.625Z"
                  stroke="#04319C"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
              </svg>
              +99365668354
            </p>
            <p>
              <svg
                width="25"
                height="25"
                viewBox="0 0 25 25"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M21.875 10.4167C21.875 17.7083 12.5 23.9583 12.5 23.9583C12.5 23.9583 3.125 17.7083 3.125 10.4167C3.125 7.93026 4.11272 5.54569 5.87087 3.78754C7.62903 2.02939 10.0136 1.04167 12.5 1.04167C14.9864 1.04167 17.371 2.02939 19.1291 3.78754C20.8873 5.54569 21.875 7.93026 21.875 10.4167Z"
                  stroke="#04319C"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
                <path
                  d="M12.5 13.5417C14.2259 13.5417 15.625 12.1426 15.625 10.4167C15.625 8.69078 14.2259 7.29167 12.5 7.29167C10.7741 7.29167 9.375 8.69078 9.375 10.4167C9.375 12.1426 10.7741 13.5417 12.5 13.5417Z"
                  stroke="#04319C"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
              </svg>
             {{$tt('Aşgabat ş., G.Bäşimow köçesi,j. 93','г. Ашхабад, улица Г. Башимова, в. 93')}}
            </p>
            <p>
              <svg
                width="25"
                height="25"
                viewBox="0 0 25 25"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M4.16683 4.16667H20.8335C21.9793 4.16667 22.9168 5.10417 22.9168 6.25V18.75C22.9168 19.8958 21.9793 20.8333 20.8335 20.8333H4.16683C3.021 20.8333 2.0835 19.8958 2.0835 18.75V6.25C2.0835 5.10417 3.021 4.16667 4.16683 4.16667Z"
                  stroke="#04319C"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
                <path
                  d="M22.9168 6.25L12.5002 13.5417L2.0835 6.25"
                  stroke="#04319C"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
              </svg>
              hosh.hyzmat@gmail.com
            </p>
          </div>
        </div>
      </div>
    </section>
    <footer>
      <div class="img">
        <img src="./../assets/image/footer.svg" alt="" />
      </div>
      <div class="contacts">
        <h1>{{$tt('Habarlaşmak üçin:','Cвязаться с нами:')}}</h1>
        <p>
          <svg
            width="25"
            height="25"
            viewBox="0 0 25 25"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M15.6769 5.20833C16.6943 5.40684 17.6294 5.90443 18.3624 6.63743C19.0954 7.37043 19.593 8.30548 19.7915 9.32291M15.6769 1.04166C17.7907 1.27649 19.7619 2.2231 21.2667 3.72605C22.7716 5.229 23.7207 7.19897 23.9582 9.3125M22.9165 17.625V20.75C22.9177 21.0401 22.8582 21.3273 22.742 21.5931C22.6258 21.8589 22.4554 22.0975 22.2416 22.2936C22.0278 22.4897 21.7754 22.639 21.5006 22.732C21.2258 22.8249 20.9346 22.8594 20.6457 22.8333C17.4403 22.485 14.3613 21.3897 11.6561 19.6354C9.13923 18.0361 7.00539 15.9023 5.40608 13.3854C3.64564 10.6679 2.55008 7.57395 2.20816 4.35416C2.18213 4.06611 2.21636 3.77579 2.30868 3.50169C2.401 3.22759 2.54938 2.97572 2.74438 2.7621C2.93937 2.54849 3.17671 2.37782 3.44128 2.26096C3.70585 2.1441 3.99185 2.0836 4.28108 2.08333H7.40608C7.91161 2.07836 8.4017 2.25737 8.785 2.58701C9.1683 2.91665 9.41866 3.37442 9.48941 3.875C9.62131 4.87507 9.86592 5.857 10.2186 6.80208C10.3587 7.17492 10.3891 7.58012 10.306 7.96966C10.2229 8.35921 10.0299 8.71678 9.74983 9L8.42691 10.3229C9.90978 12.9308 12.0691 15.09 14.6769 16.5729L15.9998 15.25C16.283 14.9699 16.6406 14.7769 17.0302 14.6938C17.4197 14.6108 17.8249 14.6411 18.1977 14.7812C19.1428 15.1339 20.1248 15.3785 21.1248 15.5104C21.6308 15.5818 22.093 15.8367 22.4233 16.2266C22.7536 16.6164 22.9292 17.1141 22.9165 17.625Z"
              stroke="#FC6604"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
          </svg>
          +99365668354
        </p>
        <p>
          <svg
            width="25"
            height="25"
            viewBox="0 0 25 25"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M21.875 10.4167C21.875 17.7083 12.5 23.9583 12.5 23.9583C12.5 23.9583 3.125 17.7083 3.125 10.4167C3.125 7.93026 4.11272 5.54569 5.87087 3.78754C7.62903 2.02939 10.0136 1.04167 12.5 1.04167C14.9864 1.04167 17.371 2.02939 19.1291 3.78754C20.8873 5.54569 21.875 7.93026 21.875 10.4167Z"
              stroke="#FC6604"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
            <path
              d="M12.5 13.5417C14.2259 13.5417 15.625 12.1426 15.625 10.4167C15.625 8.69078 14.2259 7.29167 12.5 7.29167C10.7741 7.29167 9.375 8.69078 9.375 10.4167C9.375 12.1426 10.7741 13.5417 12.5 13.5417Z"
              stroke="#FC6604"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
          </svg>
          {{$tt('Aşgabat ş., G.Bäşimow köçesi,j. 93','г. Ашхабад, улица Г. Башимова, в. 93')}}
        </p>
        <p>
          <svg
            width="25"
            height="25"
            viewBox="0 0 25 25"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M4.16683 4.16667H20.8335C21.9793 4.16667 22.9168 5.10417 22.9168 6.25V18.75C22.9168 19.8958 21.9793 20.8333 20.8335 20.8333H4.16683C3.021 20.8333 2.0835 19.8958 2.0835 18.75V6.25C2.0835 5.10417 3.021 4.16667 4.16683 4.16667Z"
              stroke="#FC6604"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
            <path
              d="M22.9168 6.25L12.5002 13.5417L2.0835 6.25"
              stroke="#FC6604"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
          </svg>
          hosh.hyzmat@gmail.com
        </p>
      </div>
      <div class="img1">
        <img src="./../assets/image/footer2.svg" alt="" />
      </div>
    </footer>
  </section>
</template>

<script>
import {
  Hooper,
  Slide,
  Progress as HooperProgress,
  Pagination as HooperPagination,
  Navigation as HooperNavigation,
} from "hooper";
import "hooper/dist/hooper.css";
import Card from "@/components/card/index.vue";

export default {
  components: {
    Hooper,
    Slide,
    HooperProgress,
    HooperPagination,
    HooperNavigation,
    Card,
  },
  data() {
   const tur =  [
        {
          id: 1,
          img: "card1.svg",
          text_tm: "Soňky minutda gezelençler",
          text_ru: "Горящие туры",
        },
        {
          id: 2,
          img: "card1.svg",
          text_tm: "Aýdyn gijeler",
          text_ru: "Ясные ночи",
        },
        {
          id: 3,
          img: "card2.svg",
          text_tm: "all inclusive",
          text_ru: "Все включено",

        },
        {
          id: 4,
          img: "card3.svg",
          text_tm: "Soňky minutda gezelençler",
          text_ru: "Горящие туры",

        },
        {
          id: 5,
          img: "slide5.jpg",
          text_tm: "Aýdyn gijeler",
          text_ru: "Ясные ночи",

        },
        {
          id: 6,
          img: "slide2.svg",
          text_tm: "all inclusive",
          text_ru: "Все включено",

        },
        {
          id: 7,
          img: "slide2.svg",
          text_tm: "Soňky minutda gezelençler",
          text_ru: "Горящие туры",

        },
        {
          id: 8,
          img: "slide2.svg",
          text_tm: "Soňky minutda gezelençler",
          text_ru: "Горящие туры",

        },
      ];
    return {
      tur,
    };
  },
  computed: {
    hooperSettings() {
      const settings = {
        itemsTOShow: 1,
        centerMode: false,
        autoPlay: true,
        playSpeed: 5000,
        transition: 1100,
        hoverPause: false,
        infiniteScroll: true,
        wheelControl: false,
      };
      return settings;
    },
  },
};
</script>
