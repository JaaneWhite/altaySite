<template>
 <header>
   <b-row >
     <b-container class="header-container">
       <b-row class="header-top-row">
         <b-col cols="0" md="2" xl="2" class="logo-block">
           <b-img src="~/assets/img/logo.png" class="logo-img"></b-img>
         </b-col>
         <b-col cols="0" md="10" xl="10" class="header-title-block">
           <b-row class="title-row">
             <b-col cols="12" md="8" xl="9" class="title-text">
               <b-row class="md">Архивы алтайского края</b-row>
               <b-row class="sm">ГААК</b-row>
             </b-col>
             <b-col cols="12" md="0" xl="3" class="login-block">
               <b-row class="login-title">
                 Авторизуйтесь для получения услуг архива
               </b-row>
               <b-row>
                 <b-col cols="4" xl="4" class="login-links search">
                   <b-button to="" class="search-link">Поиск по сайту</b-button>

                 </b-col>
                 <b-col cols="8" xl="8" class="login-links auth">
                   <b-dropdown text="Вход или регистрация"
                               class="auth-button">
                     <b-dropdown-item href="#">Вход</b-dropdown-item>
                     <b-dropdown-item href="#">Регистрация</b-dropdown-item>
                   </b-dropdown>

                 </b-col>
               </b-row>
             </b-col>
           </b-row>
           <b-row class="menu-row">
            <top-menu />
           </b-row>
         </b-col>
       </b-row>
     </b-container>
   </b-row>
 </header>
</template>

<script>
import TopMenu from "~/components/TopMenu";
export default {
  name: "HeaderComponent",
  components: {TopMenu}
}
</script>

<style lang="scss">
/* по умолчанию -  мобильная версия - 0 - 767 px*/
@media (min-width: 0) {
  .header-top-row {
    .logo-block {
      display: none;
      padding: 0;

      .logo-img {
        margin: auto;
        width: 100%;
      }
    }
    .header-title-block {
      padding: 0;
      display: flex;
      flex-direction: row;
      justify-content: space-between;

      .title-row {
        .title-text {
          display: none;
        }
        .login-block {
          display: none;
        }
      }
      .menu-row {
        width: 100%
      }
    }
  }
}
/* планшетная версия - 768 - 1023 px*/
@media (min-width: 768px) {
  .header-container {
    width: 100%;
    max-width: none;
  }
  .header-top-row {
    .logo-block {
      display: flex;
      padding: 0;

      .logo-img {
        margin: 30px auto;
        width: auto;
      }
    }
    .header-title-block {
      padding: 0;
      display: flex;
      flex-direction: row;
      justify-content: space-between;
      .title-row {
        .title-text {
          padding-left: 15px;
          display: flex;
          font-family: 'Oswald', sans-serif;
          font-size: 24px;
          font-weight: bold;
          text-transform: uppercase;
          line-height: 1.5;
          text-align: left;
          margin-top: auto;
          margin-bottom: auto;
          .sm {
            display:none;
          }
          .md {
            display: flex;
          }
        }
        .login-block {
          text-align: right;
          padding: 0 15px;
          margin-top: 15px;
          color: #aab2b5;
          .login-title {
            font-style: italic;
            font-size: 13px;
            display: block;
            text-align: right;
            padding-bottom: 10px;
          }
        }
        &.search {
          padding-left: 25px;
          background-image: url("~assets/img/search.png");
          background-position: left;
          background-repeat: no-repeat;
          background-size: 20%;
          text-align: left;
          .search-link {
            font-size: 13px;
            text-decoration: none;
            text-align: left;
            background-color: transparent !important;
            border-radius: 0;
            border: none;
            padding: 0;
            box-shadow: none;
            border-bottom: dotted 2px #343f44;
            &:hover {
              border-bottom: solid 2px #9783a6;
            }
          }
        }
        &.auth {
          text-align: right;
          background-image: url("~assets/img/arrow down.png");
          background-position: right;
          background-repeat: no-repeat;
          background-size: 5%;
          &:hover {
            background-image: url("~assets/img/arrow down w.png");
            background-position: right;
            background-repeat: no-repeat;
            background-size: 5%;
          }
          .auth-button {
            .btn-secondary {
              font-size: 13px;
              background-color: transparent !important;
              border-radius: 0;
              border: none;
              padding: 0;
              color: #343f44;
              box-shadow: none;
              border-bottom: dotted 2px #343f44;
              &:hover {
                color: #9783a6;
                border-bottom: dotted 2px #9783a6;
              }
            }
            .dropdown-toggle::after {
              display: none;
            }
          }
        }
      }
      .menu-row {
        width: 50%;
      }
    }
  }
}
/* ПК версия -  от 1024 px*/
@media (min-width: 1024px) {
  .header-container {
    max-width: 1140px;
  }
  .header-top-row {
    .logo-block {
      display: flex;
      .logo-img {
        width: 110px;
        height: 110px;
        margin-left: 0;
      }
    }
    .header-title-block {
      padding: 0;
      flex-direction: column;
      .title-row {
        .title-text {
          margin-top: 30px;
          display: flex;
          .md {
            display: flex;
          }
        }
        .login-block {
          display: block;
          padding: 0;
          .login-title {
            padding-bottom: 10px;
          }
        }
        & .cart {
          .cart-link {
            font-size: 14px;
          }
        }
        & .auth {
          .auth-button {
            .btn-secondary {
              font-size: 14px;
            }
          }
        }
      }
      .menu-row {
        width: 100%;
      }
    }
  }
}

</style>
