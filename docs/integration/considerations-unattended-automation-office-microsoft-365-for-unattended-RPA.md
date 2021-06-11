---
title: Consideraciones para la automatización desatendida de Office en el Microsoft 365 entorno de RPA desatendido
ms.date: 03/30/2020
ms.audience: Developer
localization_priority: Normal
description: Consideraciones para la automatización desatendida de Office en el Microsoft 365 entorno de RPA desatendido.
ms.openlocfilehash: 576217fc85f2980a6d2451e3f930296ea4c11a56
ms.sourcegitcommit: 007aa2ceb4f569201c3f4372de5c83b6c61f8875
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2020
ms.locfileid: "43103053"
---
# <a name="considerations-for-unattended-automation-of-office-in-the-microsoft-365-for-unattended-rpa-environment"></a>Consideraciones para la automatización desatendida de Office en el Microsoft 365 entorno de RPA desatendido

Aunque Microsoft 365 para RPA desatendida proporciona una licencia que permite la automatización de Office sin ningún usuario presente, todas las versiones actuales de Office se diseñaron y probaron para ejecutarse como productos de usuario final en una estación de trabajo cliente con un usuario presente para interactuar con la interfaz de la aplicación. Los comportamientos inesperados resultantes del uso de aplicaciones sin un usuario presente no son defectos. Si desea ejecutar Office en esta configuración, debe estar preparado para tener en cuenta estos comportamientos inesperados en la lógica de la aplicación.

En este artículo se describen algunas de las consideraciones para la automatización desatendida de Office para ayudarle si usa este enfoque. Sin embargo, tenga en cuenta que el uso de Office en esta configuración es estrictamente "AS IS" y debe tener en cuenta estos comportamientos inesperados. La información que se proporciona aquí no es exhaustiva y no se garantiza que resuelva todos los problemas de todos los clientes. Le recomendamos que pruebe la solución exhaustivamente antes de implementarla.

## <a name="common-problems-in-unattended-automation"></a>Problemas comunes en la automatización desatendida

Si desea usar Office sin un usuario presente, tenga en cuenta las siguientes áreas en las que Office puede comportarse de forma diferente de lo esperado. Para que la solución se ejecute correctamente, debe solucionar estos problemas y minimizar sus efectos tanto como sea posible. Tenga en cuenta estos problemas cuidadosamente al compilar la aplicación.

### <a name="interactive-ui-elements"></a>Elementos de interfaz de usuario interactivos

Office las aplicaciones suponen que se ejecutan de forma interactiva. Si se produce un error inesperado o si se necesita un parámetro no especificado para completar una función, Office está diseñado para solicitar al usuario un cuadro de diálogo que le pregunte al usuario cómo desea continuar. En la automatización desatendida, esto puede provocar que la aplicación parezca "colgar" mientras la aplicación se detiene hasta que recibe esta entrada. Si va a automatizar Office a través de sus API públicas, puede suprimir muchas de estas alertas configurando propiedades como [Application.DisplayAlerts](https://docs.microsoft.com/office/vba/api/word.application.displayalerts) y [Application.AutomationSecurity](https://docs.microsoft.com/office/vba/api/word.application.automationsecurity) adecuadamente. El código debe estar diseñado para identificar y procesar alertas de bloqueo en cualquier momento.

### <a name="user-identity"></a>Identidad de usuario

Office aplicaciones requieren una identidad de usuario cuando se ejecutan las aplicaciones, incluso cuando la aplicación se inicia a través de la automatización. Esta identidad de usuario puede provocar cualquiera o todas las siguientes causas:

- La presencia de la interfaz de usuario de inicio de sesión adicional que debe controlarse.
- Archivos que no se pueden abrir ni editar en función de los permisos de acceso por usuario.
- Cambios inesperados en los metadatos del archivo (por ejemplo, determinadas propiedades de archivo se actualizarán en función de la identidad de la identidad de usuario de la instancia de aplicación automatizada).

Varios enfoques pueden ayudar a mitigar estos problemas; por ejemplo, ejecutar el [Inspector de documentos](https://docs.microsoft.com/office/vba/library-reference/concepts/using-the-document-inspector) para quitar metadatos. Tenga en cuenta si estos enfoques son adecuados en función del escenario.

### <a name="server-side-security"></a>Seguridad del lado servidor

Al ejecutar Office desatendido y procesar contenido de archivos arbitrarios, no hay protecciones adicionales específicas en ese entorno disponibles para impedir que las macros almacenadas en esos archivos se carguen y ejecuten. Office no le protege de la ejecución involuntara de macros desde el código o de iniciar otro servidor que pueda ejecutar macros. Puede usar propiedades como [Application.AutomationSecurity](https://docs.microsoft.com/office/vba/api/word.application.automationsecurity) para mitigar este riesgo, pero debe asegurarse de que solo está cargando contenido de confianza.

Además, Office muchos componentes (como MAPI simple, WinInet y MSDAIPP) que pueden almacenar en caché la información de autenticación de cliente para acelerar el procesamiento. Cuando Office de servidor automatizado y procesa varios archivos, si la información de autenticación se ha almacenado en caché para esa sesión, un cliente puede usar las credenciales almacenadas en caché de otro cliente. Por lo tanto, el cliente puede obtener permisos de acceso no concedidos suplantando a otros usuarios.

### <a name="ui-changes"></a>Cambios en la interfaz de usuario

Los elementos de la interfaz de usuario de Office son en gran medida estables, pero la ubicación específica de cualquier elemento de la interfaz de usuario no está garantizada y puede cambiar a medida que el diseño del producto evoluciona para incorporar los comentarios de los usuarios y satisfacer las necesidades del cliente. La lógica de cualquier automatización debe tener en cuenta esto. Estos cambios pueden dar lugar a cambios de nomenclatura de pestañas de botones o grupos, movimiento de comandos entre pestañas, adición de pestañas nuevas o eliminación de comandos en alineación con nuestras directivas de desuso de características. Estos cambios pueden tener lugar en la interfaz de usuario, así como en la información de accesibilidad proporcionada por la aplicación, ya que esa información se modifica para mejorar la facilidad de uso y tener en cuenta los comentarios continuos de los clientes, y pueden ser lanzados para diferentes usuarios en diferentes momentos.

Incluso sin cambios en el producto, las diferencias entre entornos del sistema (como el tamaño de pantalla/resolución/PPP) pueden provocar cambios en la ubicación de los elementos en pantalla. Cualquier enfoque que se base en coordenadas de pantalla para simular la entrada del usuario debe tener en cuenta estos cambios y adaptarse en consecuencia.

### <a name="single-threading"></a>Subproceso único

Office son aplicaciones no reenentrantes basadas en STA diseñadas para proporcionar una funcionalidad diversa pero que consume muchos recursos para un solo cliente. Las aplicaciones usan recursos globales como archivos asignados a memoria, complementos globales o plantillas y servidores de automatización compartidos. Esto puede limitar el número de instancias que se pueden ejecutar simultáneamente y pueden provocar condiciones de carrera si las aplicaciones están configuradas en un entorno multicliente. Si tiene previsto ejecutar más de una instancia de cualquier aplicación Office, debe planear aislarlas en el nivel de la máquina virtual para garantizar la estabilidad de la solución resultante.

### <a name="resiliency-and-stability"></a>Resistencia y estabilidad

Incluso con las consideraciones anteriores, si las aplicaciones están automatizadas de formas que simulan la entrada del usuario o de longitudes de sesión que superan considerablemente el uso interactivo, podrían encontrarse con problemas que no están presentes cuando se ejecutan de forma interactiva. Las soluciones que usan Office en este contexto deben crear de forma proactiva mecanismos para supervisar el estado de la aplicación y reiniciarlas (o la máquina virtual en la que se ejecutan) si es necesario.

## <a name="suggested-alternatives"></a>Alternativas sugeridas

Microsoft recomienda encarecidamente algunas alternativas que no requieren que Office se instale y ejecute en el lado servidor, y que pueden realizar tareas comunes de forma más eficaz y rápida que la automatización en esta configuración. Antes de implicar Office como un componente del lado servidor en el proyecto, considere alternativas.

### <a name="microsoft-graph"></a>Microsoft Graph

La API de Microsoft Graph proporciona acceso a los servicios, datos e inteligencia que están disponibles para los usuarios y soluciones como parte de la nube de Microsoft, incluidos muchos servicios que admiten las necesidades de automatización desatendida: acceso al correo / calendario / contactos / archivos de los usuarios, conversión de documentos, cálculo de libro de Excel, etc. Estos servicios están diseñados para el uso desatendido y el acceso a gran escala, y usan una sintaxis estándar de LA API RESTful. Para obtener más información sobre microsoft Graph y cómo usarlo para trabajar con los datos de los usuarios, visite lo siguiente:

- [Información general de Microsoft Graph](https://docs.microsoft.com/graph/overview) 
- [Introducción a Microsoft Graph](https://developer.microsoft.com/graph/get-started)
- [Descargar un archivo en otro formato](https://docs.microsoft.com/graph/api/driveitem-get-content-format?view=graph-rest-1.0&tabs=http) (conversión de archivos)
- [Trabajar con Excel en Microsoft Graph](https://docs.microsoft.com/graph/api/resources/excel?view=graph-rest-1.0) (detalles del libro)

### <a name="open-xml-file-formats"></a>Formatos de archivo Open XML

Muchas tareas de automatización implican la creación o edición de documentos. Office admite formatos de archivo Open XML que permiten a los desarrolladores crear, editar, leer y transformar contenido de archivos con tecnologías XML y ZIP estándar, definidas en el estándar internacional ISO 29500. Estos formatos de archivo se pueden manipular a través de cualquier herramienta ZIP/XML, incluido el espacio de nombres System.IO.Package.IO en Microsoft .NET 3.x Framework. La edición directa de los formatos de archivo es el método recomendado y compatible para controlar los cambios en Office archivos de un servicio.

Microsoft proporciona un SDK para manipular formatos de archivo Open XML desde .NET 3.x Framework. Para obtener más información sobre el SDK y cómo usar el SDK para crear o editar archivos Open XML, visite lo siguiente:

- [Descripción de los formatos de archivo Open XML](https://docs.microsoft.com/office/open-xml/understanding-the-open-xml-file-formats)
- [Bienvenido a Open XML SDK 2.5 para Office](https://docs.microsoft.com/office/open-xml/open-xml-sdk)
