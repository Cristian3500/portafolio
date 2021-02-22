<template>
  <div class="home">

    <v-img
      dark
      max-height="500px"
      src="https://images.unsplash.com/photo-1505238680356-667803448bb6?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1050&q=80"
    >
      <v-layout fill-height align-center>
        <v-container>
          <v-row align="center" justify="center" class="white--text">
            <v-col cols="12">
              <div
                :class="{'display-2 font-weight-bold ': $vuetify.breakpoint.smAndUp, 'title font-weight-bold': $vuetify.breakpoint.smAndDown}"
              >Bienvenido a mi página.</div>
              <div
                :class="{'headline': $vuetify.breakpoint.smAndUp, 'subtitle-1': $vuetify.breakpoint.smAndDown}"
              >Programador Full Stack</div>
            </v-col>
          </v-row>
        </v-container>
      </v-layout>
    </v-img>
    <v-container class="mt-5">
      <v-layout wrap>
        <v-flex xs12>
          <div class="display-1 font-weight-bold" id="about">Acerca de mi</div>
        </v-flex>
        <v-flex xs12 mt-5>
          <div class="body-1">{{aboutText}}</div>
          <div
            class="body-1 mt-3"
          >Me gustaria hablar con ustedes, escuchar sus ideas y que puedan comprobar mi experiencia.</div>
        </v-flex>
      </v-layout>
      <v-layout wrap my-5>
        <v-flex xs12>
          <div class="display-1 font-weight-bold" id="portfolio">Mis Trabajos</div>
        </v-flex>
        <v-flex xs12 class="mt-5">
          <v-layout wrap>
            <template v-for="(app, i) in apps">
              <v-flex :key="i" xs12 sm6 md4>
                <p-portfolio-app :app="app" />
              </v-flex>
            </template>
          </v-layout>
        </v-flex>
      </v-layout>
      <v-layout wrap my-5>
        <v-flex xs12 mb-5>
          <div class="display-1 font-weight-bold" id="contact">Contactame ...</div>
        </v-flex>
        <template v-for="(contact, i) in contactLinks">
          <v-flex sm6 md4 xs12 :key="i">
            <p-contact-info :contact="contact" />
          </v-flex>
        </template>
      </v-layout>
      <!-- <v-layout wrap my-5>
        <v-flex xs12>
          <div class="display-1 font-weight-bold">Press</div>
        </v-flex>
        <v-flex xs12>
          <v-layout>
            <v-card width="">
              <v-card-title>Press card</v-card-title>
            </v-card>
          </v-layout>
        </v-flex>
      </v-layout>-->
    </v-container>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";
import PPortfolioApp from "@/components/PPortfolioApp.vue";
import PContactInfo from "@/components/PContactInfo.vue";

export default {
  name: "home",
  components: {
    PPortfolioApp,
    PContactInfo
  },
  data() {
    return {
      aboutText:
        "Hola gracias por visitar mi sitio, espero que me puedan tomar en cuenta con mucho gusto presento mis proyectos y los animó a que puedan evaluar mis conocimientos, he dirigido varios proyectos. Se  programar en varios lenguajes haciendo uso de varios frameworks como Laravel, Vue JS, Angular, .Net Core, Java. Se trabajar en equipo, he trabajado con varias herramientas y metodologías de desarrollo ágil como SCRUM, KANBAN. Tengo experiencia en el ámbito de dirección de proyecto y como programador, se que puedo aportar en la organización que representan. En el tema de desarrollo de aplicaciones móviles he desarrollado aplicaciones en IONIC y QUASAR.",
      apps: [
        {
          name: "Mercado Goblal",
          price: "Finalizado",
          logo: "sigemg.png",
          platforms: [
            {
              name: "Sigemg",
              link: "https://sigemg.com/"
            }
          ],
          description:
            "Sistema desarrollado para la ONG denominada Mercado Global, con el objetivo de controlar y gestionar: capacitaciones, control de asistecia, control de calidad, producción, ahorros y otras caracteristicas de ulitidad para la ONG. El sistema esta desarrollado con el framework Laravel y como motor de base datos utilice MySQL.",
          technologies: [
            {
              name: "Laravel",
              icon: "mdi-laravel",
              link: "https://laravel.com/"
            },
            {
              name: "MySQL",
              icon: "mdi-database",
              link: "https://www.mysql.com/"
            }
            ,
            {
              name: "Bitbucket",
              icon: "mdi-bitbucket",
              link: "https://bitbucket.org/"
            }
          ],
          code: {
            name: "github",
            icon: "mdi-github",
            link: ""
          }
        },
        {
          name: "Soloconta Sololá",
          price: "Finalizado",
          logo: "soloconta.png",
          platforms: [
            {
              name: "Soloconta",
              link: "https://soloconta.sistemastc.com/"
            }
          ],
          description:
            "Sistema desarrollado como un producto propio para ofrecer a diferentes tipos de empresas, el sistemas cuenta con punto de venta, cobro de servicios facturados mensualmente o de manera indeterminada, manejo de clientes, informes, gastos, proveedores y otros elementos; para una empresa de servicios o venta de bienes, se le provee al cliente un subdominio y el alojamiento de sus datos a cambio de un pago anual. Utilizo como dominio principal Sistemastc.com",
          technologies: [
            {
              name: "VueJS",
              icon: "mdi-vuejs",
              link: "https://vuejs.org/"
            },
            {
              name: "Laravel",
              icon: "mdi-laravel",
              link: "https://laravel.com/"
            },
            {
              name: "MySQL",
              icon: "mdi-database",
              link: "https://www.mysql.com/"
            }
            ,
            {
              name: "Bitbucket",
              icon: "mdi-bitbucket",
              link: "https://bitbucket.org/"
            }
          ],
          code: {
            name: "github",
            icon: "mdi-github"
          }
        },
        {
          name: "MAB",
          price: "Finalizado",
          logo: "mab.png",
          platforms: [
            {
              name: "MAB",
              link: "https://drive.google.com/file/d/1-ZvDTXQvZznCl25fKiIpD1B7j-U7VcJH/view?usp=sharing"
            }
          ],
          description:
            "MAB (Master Bussines Admnistrator), proyecto propio, este sistema tiene como objetivos: ser de apoyo en la administración de la empresa, ser un soporte fiable para la toma de decisiones y mejorar la eficiencia en los procesos. Logrando así una mejora en la calidad de servicio a los diferentes departamentos dentro de la empresa y a sus clientes.",
          technologies: [
            {
              name: "Java",
              icon: "mdi-language-java",
              link: ""
            },
            {
              name: "MySQL",
              icon: "mdi-database",
              link: "https://www.mysql.com/"
            },
            {
              name: "Bitbucket",
              icon: "mdi-bitbucket",
              link: "https://bitbucket.org/"
            },
          ],
          code: {
            name: "github",
            icon: "mdi-github",
            link: ""
          }
        },
        {
          name: "Bugonet",
          price: "En proceso",
          logo: "bugonetiso.png",
          platforms: [
            {
              name: "Bugonet"
            }
          ],
          description:
            "Proyecto propio realizado desarrollado en .Net Core como backend, utilizando la arquitectura de repositorio para la capa de datos, y MVC; en el fronted utilice Angular. Sistema permite realizar publicaciones de productos para venta de manera sencilla y realizar compras de manera sencilla, para empresas con entrega a domicilio. Cuenta con web socket de SignalR para varios servicios del sistema, así como autenticación por Firebase.",
          technologies: [
            {
              name: "Angular",
              icon: "mdi-angular",
              link: "https://angular.io/"
            },
            {
              name: ".Net Core",
              icon: "mdi-language-csharp",
              link: "https://dotnet.microsoft.com/"

            },
            {
              name: "MySQL",
              icon: "mdi-database",
              link: "https://www.mysql.com/"
            },
            {
              name: "Firebase",
              icon: "mdi-firebase",
              link: "https://firebase.google.com/?hl=es"
            },
            {
              name: "Azure DevOps",
              icon: "mdi-microsoft-azure-devops",
              link: "https://azure.microsoft.com/es-mx/services/devops/"
            },
            {
              name: "Bitbucket",
              icon: "mdi-bitbucket",
              link: "https://bitbucket.org/"
            },
            {
              name: "Azure",
              icon: "mdi-microsoft-azure",
              link: "https://azure.microsoft.com/"
            }
          ],
          code: {
            name: "github",
            icon: "mdi-github",
          }
        },
        {
          name: "Ubiquemos",
          price: "Finalizado",
          logo: "ubiquemos.png",
          platforms: [
            {
              name: "Ubiquemos"
            }
          ],
          description:
            "Sistema creado para la municipalidad de San Andres Semetabaj, Sololá. Este sistema tenia como fin controlar los ingresos de las personas en centro comerciales, mercados etc. con el fin de determinar posibles brotes de Covid-19, de tal manera que les permita identificar a los posibles infectados, asi mismo tener un control estricto durantes los toques de queda.",
          technologies: [
            {
              name: "VueJS",
              icon: "mdi-vuejs",
              link: "https://vuejs.org/"
            },
            {
              name: "Laravel",
              icon: "mdi-laravel",
              link: "https://vuetifyjs.com/"
            },
            {
              name: "MySQL",
              icon: "mdi-database",
              link: "https://www.mysql.com/"
            }
          ],
          code: {
            name: "github",
            icon: "mdi-github",
            link: "https://github.com/"
          }
        },
        {
          name: "Super Cable",
          price: "Finalizado",
          logo: "supercable.png",
          platforms: [
            {
              name: "Supercable",
            }
          ],
          description:
            "Sistema desarrollado para la empresa Super Cable del municipio de Argueta, del departamento de Sololá, el sistema le permite a la empresa llevar el control de pagos de sus clientes, otros ingresos, egresos y planilla, el sistema lo desarrolle en Java usando MySQL como motor de base de datos.",
          technologies: [
            {
              name: "Java",
              icon: "mdi-language-java",
              link: ""
            },
            {
              name: "MySQL",
              icon: "mdi-database",
              link: "https://www.mysql.com/"
            },
            {
              name: "Bitbucket",
              icon: "mdi-bitbucket",
              link: "https://bitbucket.org/"
            },
          ],
          code: {
            name: "github",
            icon: "mdi-github",
            link: "https://github.com/"
          }
        },
        {
          name: "Servidores",
          price: "Finalizado",
          logo: "vps.png",
          platforms: [
            {
              name: "web",
              icon: "mdi-web",
              link: "https:/www.google.com/"
            }
          ],
          description:
            "Experiencia configurando servidores con los siguientes sistemas operativos: Windows Server, Ubuntu, Centos. Manejo de Docker, Nginx, Nginx Proxy.",
          technologies: [
            {
              name: "Docker",
              icon: "mdi-docker",
              link: "https://vuejs.org/"
            },
            {
              name: "Linux",
              icon: "mdi-linux"
            },
            {
              name: "Windows Server",
              icon: "mdi-microsoft-windows"
            }
          ],
          code: {
            name: "github",
            icon: "mdi-github"
          }
        }
      ],
      contactLinks: [
        {
          name: "Email",
          value: "neftaligarcia3500@gmail.com",
          link: "mailto:neftaligarcia3500@gmail.com",
          icon: "mdi-email"
        },
        {
          name: "Telefono",
          value: "+(502) 4240-4715",
          link: "tel:+50242404715",
          icon: "mdi-phone"
        },
        {
          name: "Facebook",
          value: "Neftalí García López",
          link: "https://www.facebook.com/",
          icon: "mdi-facebook"
        },
        {
          name: "Whatsapp",
          value: "+(502) 4240-4715",
          link: "whatsapp://send?text=Hola Neftalí, he visto tu portafolio&phone=+50242404715&abid=+50242404715",
          icon: "mdi-whatsapp"
        }
      ]
    };
  }
};
</script>
