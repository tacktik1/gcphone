<h2 align="center">Telefono FiveM</h2>

![Image of gcphone1](https://i.imgur.com/naTiBgI.png)
![Image of gcphone2](https://i.imgur.com/LAicovK.png)
![Image of gcphone4](https://i.imgur.com/rzWdDMy.png)
![Image of gcphone5](https://i.imgur.com/9h7eiI8.png)

## Funcionalidades 
  - Lista de contactos
  - Envio de sms
  - Llamar
  - Llamada Anonima
  - Aplicacion Banco
  - Aplicacion Chat Anonimo
  - Aplicacion Bolsa



### Modificar el fichero /html/static/config/config.json
```json
{
  "//": "Nom du reseau situé dans la barre du téléphone",
  "reseau": "Gannon",
  
  "//": "Color base del telefono",
  "themeColor": "#303f9f",

  "//": "Lista de colores contactos",
  "colors": [
    "#EF5350",
    "#EC407A",
    "#AB47BC",
    "#7E57C2",
    "#5C6BC0",
    "#42A5F5",
    "#29B6F6",
    "#26C6DA",
    "#26A69A",
    "#66BB6A",
    "#9CCC65",
    "#D4E157",
    "#FFCA28",
    "#FFA726",
    "#FF7043",
    "#8D6E63",
    "#78909C"
  ],

  "//": "Si false, Ajoute un '-' dans le numero (###-####)",
  "useFormatNumberFrance": false,

  "//": "useWebRTCVocal: false => Appels avec channels de GTA",
  "//": "useWebRTCVocal: true  => Appels avec WebRTC",
  "useWebRTCVocal": true,

  "//": "Configuration des serveurs TURN à utilisé",
  "RTCConfig": {
    "iceServers": [{
      "urls": ["turn:gannon.ovh"],
      "username": "jojo",
      "credential": "pass"
    }]
  },


  "//": "Lista fondos disponibles, location => /html/static/img/background",
  "background" : {
    "Calvin & Hobbes": "back001.jpg",
    "Destiny": "back002.jpg",
    "Stormtrooper": "back003.jpg",
    "Custom URL": "URL"
  },
  "//": "Fuente por defecto",
  "background_default": {
    "label": "Calvin & Hobbes",
    "value": "back001.jpg"
  },

  "//": "Lista de telofonos, location => /html/static/img/coque",
  "coque": {
    "Sansumg S8": "s8.png",
    "Iphone X": "iphonex.png",
    "Brick Base": "base.png",
    "Transparent": "transparent.png"
  },
  "//": "Telefono por defecto",
  "coque_default": {
    "label": "Sansumg S8",
    "value": "s8.png"
  },

  " // " : " Configuración de llamada de servicio (favorito) " ,
   " serviceCall " : [
    {

      " // " : " Nombre del elemento " ,
       " pantalla " : " Fuente " ,

      " // " : " Opcional: color de la ficha " ,
       " backgroundColor " : " rojo " ,

      " // " : " Opcional: Imagen del chip " ,
       " icon " : " /html/static/img/icons_app/bank.png " ,

      " // " : " Lista de acciones disponibles " ,
       " subMenú " : [
        {
          " // " : " Título de la acción " ,
           " título " : " Enviar un mensaje " ,

          " // " : " Nombre del activador del evento cuando se usa " ,
           " eventName " : " esx_addons_gcphone: call " ,

          " // " : " Opcional: parámetro 'datos' enviado con el evento " ,
           " tipo " : {
             " número " : " policía "
          }
        },
        {
          " title " : " Centralita de llamadas " ,
           " eventName " : " gcphone: autoCallNumber " ,
           " type " : {
             " number " : " 911 "
          }
        }
      ]
    },
    {
      " display " : " Ambulancia " ,
       " backgroundColor " : " rojo " ,
       " subMenu " : [
        {
          " title " : " Enviar mensaje " ,
           " eventName " : " esx_addons_gcphone: call " ,
           " type " : {
             " number " : " ambulance "
          }
        }
      ]
    }
  ],
  
  " // " : " Agregar contactos predeterminados " ,
   " defaultContacts " : [
    { " number " : " ambulance " , " display " : " AABBUULLAANNCCEE " , " icon " : " /html/static/img/icons_app/bank.png " },
    { " number " : " font " , " display " : " Police " , " backgroundColor " : " blue " , " letter " : " J " }
  ],

  " // " : " Configuración de la aplicación " ,
   " aplicaciones " : [
    {
      " // " : " Nombre de la aplicación " ,
       " nombre " : " Teléfono " ,

      " // " : " Iconos de la aplicación " ,
       " iconos " : " /html/static/img/icons_app/call.png " ,

      " // " : " Ruta de la aplicación, NO MODIFICAR " ,
       " routeName " : " llamadas " ,

      " // " : " Si es verdadero, la aplicación estará disponible en la página de inicio " ,
       " inHomePage " : verdadero ,

      " // " : " Si es falso, la aplicación no es visible " ,
       " habilitada " : verdadero
    },
    {
      " nombre " : " Mensajes " ,
       " iconos " : " /html/static/img/icons_app/sms.png " ,
       " routeName " : " mensajes " ,
       " inHomePage " : verdadero ,

      " // " : " Referencia a la tienda, para mostrar una viñeta debajo del icono de la aplicación " ,
       " puceRef " : " nbMessagesUnread " ,
    },
    {
      " nombre " : " Contactos " ,
       " iconos " : " /html/static/img/icons_app/contacts.png " ,
       " routeName " : " contactos " ,
       " inHomePage " : verdadero
    },
    {
      " nombre " : " Parámetros " ,
       " iconos " : " /html/static/img/icons_app/settings.png " ,
       " routeName " : " parámetro " ,
       " inHomePage " : verdadero
    },
    {
      " nombre " : " Banco " ,
       " iconos " : " /html/static/img/icons_app/bank.png " ,
       " routeName " : " banco " ,
       " inHomePage " : falso
    },
    {
      " nombre " : " Bolsa " ,
       " iconos " : " /html/static/img/icons_app/bourse.png " ,
       " routeName " : " bolsa " ,
       " habilitado " : verdadero
    },
    {
      " nombre " : " Foto " ,
       " iconos " : " /html/static/img/icons_app/photo.png " ,
       " routeName " : " foto "
    },
    {
      " nombre " : " Chat oscuro " ,
       " iconos " : " /html/static/img/icons_app/tchat.png " ,
       " routeName " : " chat "
    }
  ],
  
  " // " : " Configuración de idioma del teléfono " ,
   " idioma " : {
     " fr_FR " : {
       " NOMBRE " : " Francés " ,
       " CLAVE " : " VALOR "
    },
    " en_US " : {
       " NAME " : " Inglés " ,
       " // " : " ... "
    },
    " // " : " Otro idioma "
  }
}
```

No olvide agregar los nuevos archivos en __ressource.lua

Puede modificar los sonidos en \ html \ static \ sound
Las conchas deben estar en formato 1000x500 px, el área de la pantalla está centrada en el tamaño 800 * 400
Las aplicaciones bancarias y de la bolsa de valores deben configurarse de acuerdo con sus scripts
Los teléfonos fijos se pueden configurar en gcphone / config.lua
- [[
   Tenga cuidado de no usar un número que entre en conflicto con un jugador 
- ]] 
FixePhone = {
   - Estación de policía 
  [ ' 911 ' ] = {name =   " Central Police " , coords = {x =  441.2 , y =  - 979.7 , z =  30,58 }},
  
  - Cabina cerca de la estación de policía 
  [ ' 008-0001 ' ] = {name =  " Cabina telefónica " , coords = {x =  372.25 , y =  - 965.75 , z =  28.58 }},
}

## Acerca de esx_addons_gcphone
Permet de faire la liaison entre le téléphone et les métiers esx.

Pon mettre esx_addons_gcphone & gcphone antes de jobs.
Ejemplo :
```yml
  # ...

  start mysql-async
  start essentialmode
  start esplugin_mysql
  start es_extended

  start esx_addons_gcphone
  start gcphone

  start esx_mecanojob
  start esx_job2
  start esx_job3
  # ...
```

## License
[GNU v3](https://opensource.org/licenses/gpl-3.0.html)
