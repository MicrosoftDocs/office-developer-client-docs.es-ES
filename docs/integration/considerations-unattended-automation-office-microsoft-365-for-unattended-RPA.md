---
title: Consideraciones para la automatización desatendida de Office en Microsoft 365 para el entorno de RPA desatendida
ms.date: 03/30/2020
ms.audience: Developer
localization_priority: Normal
description: Consideraciones para la automatización desatendida de Office en Microsoft 365 para el entorno de RPA desatendida.
ms.openlocfilehash: 576217fc85f2980a6d2451e3f930296ea4c11a56
ms.sourcegitcommit: 007aa2ceb4f569201c3f4372de5c83b6c61f8875
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2020
ms.locfileid: "43103053"
---
# <a name="considerations-for-unattended-automation-of-office-in-the-microsoft-365-for-unattended-rpa-environment"></a>Consideraciones para la automatización desatendida de Office en Microsoft 365 para el entorno de RPA desatendida

Aunque Microsoft 365 para RPA desatendida ofrece una licencia que permite la automatización de Office sin ningún usuario, todas las versiones actuales de Office se diseñaron y probaron para ejecutarse como productos de usuario final en una estación de trabajo cliente con un usuario presente para interactuar con la interfaz de la aplicación. Los comportamientos inesperados que se derivan del uso de aplicaciones sin un usuario presente no son defectos. Si desea ejecutar Office en esta configuración, debe estar preparado para tener en cuenta estos comportamientos inesperados en la lógica de la aplicación.

En este artículo se describen algunas de las consideraciones para la automatización desatendida de Office para ayudarle si usa este método. Sin embargo, tenga en cuenta que el uso de Office en esta configuración es estrictamente "tal cual" y debe tener en cuenta estos comportamientos inesperados. La información que se proporciona aquí no es exhaustiva y no se garantiza que resuelva todos los problemas de todos los clientes. Le recomendamos que pruebe minuciosamente su solución antes de implementarla.

## <a name="common-problems-in-unattended-automation"></a>Problemas comunes en la automatización desatendida

Si desea usar Office sin un usuario presente, tenga en cuenta las siguientes áreas en las que Office puede comportarse de forma diferente a lo esperado. Para que la solución se ejecute correctamente, debe solucionar estos problemas y minimizar sus efectos lo máximo posible. Tenga en cuenta estos problemas con cuidado al compilar la aplicación.

### <a name="interactive-ui-elements"></a>Elementos interactivos de interfaz de usuario

Las aplicaciones de Office suponen que se ejecutan de forma interactiva. Si se produce un error inesperado, o si se necesita un parámetro sin especificar para completar una función, Office está diseñado para solicitar al usuario un cuadro de diálogo que le pregunte cómo desea continuar. En la automatización desatendida, esto puede hacer que la aplicación aparezca como "bloqueo" cuando la aplicación se detiene hasta que recibe esta entrada. Si está automatizando Office a través de sus API públicas, puede suprimir muchas de estas alertas mediante la configuración de propiedades como [Application. DisplayAlerts](https://docs.microsoft.com/office/vba/api/word.application.displayalerts) y [Application. AutomationSecurity](https://docs.microsoft.com/office/vba/api/word.application.automationsecurity) correctamente. El código debe diseñarse para identificar y procesar las alertas de bloqueo en cualquier momento.

### <a name="user-identity"></a>Identidad del usuario

Las aplicaciones de Office requieren una identidad de usuario cuando se ejecutan las aplicaciones, incluso cuando la aplicación se inicia a través de la automatización. La identidad de este usuario puede provocar alguna o todas las acciones siguientes:

- La presencia de interfaz de usuario de inicio de sesión adicional que se debe controlar.
- Archivos que no se pueden abrir o editar en función de los permisos de acceso por usuario.
- Cambios inesperados en los metadatos del archivo (por ejemplo, algunas propiedades de archivo se actualizarán en función de la identidad de la identidad del usuario de la instancia de la aplicación automatizada).

Varios métodos pueden ayudar a mitigar estos problemas; por ejemplo, ejecutar el [Inspector de documento](https://docs.microsoft.com/office/vba/library-reference/concepts/using-the-document-inspector) para quitar metadatos. Considere si estos enfoques son adecuados según su escenario.

### <a name="server-side-security"></a>Seguridad del servidor

Cuando se ejecuta Office de forma desatendida y se procesa contenido de archivo arbitrario, no hay disponibles protecciones adicionales específicas en ese entorno para evitar que las macros almacenadas en esos archivos se carguen y se ejecuten. Office no protege el usuario de las macros que se ejecutan involuntariamente desde el código o iniciando otro servidor que pueda ejecutar macros. Puede usar propiedades como [Application. AutomationSecurity](https://docs.microsoft.com/office/vba/api/word.application.automationsecurity) para mitigar este riesgo, pero debe asegurarse de que solo carga contenido de confianza.

Además, Office usa muchos componentes (como simple MAPI, WinInet y MSDAIPP) que pueden almacenar en caché la información de autenticación del cliente para acelerar el procesamiento. Cuando Office se encuentra automatizado en el servidor y procesando varios archivos, si se ha almacenado en caché la información de autenticación de esa sesión, un cliente puede usar las credenciales almacenadas en caché de otro cliente. Por lo tanto, el cliente puede obtener permisos de acceso no concedidos suplantando a otros usuarios.

### <a name="ui-changes"></a>Cambios en la interfaz de usuario

Los elementos de la interfaz de usuario de Office son muy estables, pero la ubicación específica de cualquier elemento de la interfaz de usuario no está garantizada y puede cambiar a medida que el diseño del producto evolucione para incorporar los comentarios de los usuarios y satisfacer las necesidades de los clientes. La lógica de cualquier automatización debe tener en cuenta esto. Estos cambios pueden dar como resultado los cambios de nombre de las fichas de botón o grupo, el movimiento de comandos entre las pestañas, la adición de nuevas pestañas o la eliminación de comandos en función de nuestras directivas de desuso de características. Estos cambios pueden tener efecto en la interfaz de usuario, así como en la información de accesibilidad proporcionada por la aplicación, ya que esta información se modifica para mejorar el uso y la cuenta para los comentarios de los clientes en curso y se puede implementar para distintos usuarios en momentos diferentes.

Incluso sin cambios en el producto, las diferencias entre los entornos del sistema (como el tamaño de pantalla/resolución/PPP) pueden dar lugar a cambios en la ubicación de los elementos en la pantalla. Cualquier método que se base en coordenadas de pantalla para simular la entrada del usuario debe considerar estos cambios y adaptarlos en consecuencia.

### <a name="single-threading"></a>Subprocesamiento único

Las aplicaciones de Office son aplicaciones no reentrantes basadas en STA que están diseñadas para proporcionar una funcionalidad diversa pero de uso intensivo de recursos para un único cliente. Las aplicaciones usan recursos globales como archivos asignados a memoria, Complementos globales o plantillas y servidores de automatización compartidos. Esto puede limitar el número de instancias que se pueden ejecutar simultáneamente y puede llevar a condiciones de carrera si las aplicaciones se configuran en un entorno multicliente. Si tiene previsto ejecutar más de una instancia de cualquier aplicación de Office, debe planear la forma de aislarlas en el nivel de la máquina virtual para garantizar la estabilidad de la solución resultante.

### <a name="resiliency-and-stability"></a>Resistencia y estabilidad

Incluso con las consideraciones anteriores, si las aplicaciones están automatizadas de manera que se simula la entrada del usuario o la duración de las sesiones que superan considerablemente el uso interactivo, es posible que se encuentren problemas que no están presentes al ejecutarse de forma interactiva. Las soluciones que usan Office en este contexto deben crear mecanismos de forma proactiva para supervisar el estado de la aplicación y reiniciarlas (o la máquina virtual en la que se están ejecutando), si es necesario.

## <a name="suggested-alternatives"></a>Sugerencias de alternativas

Microsoft recomienda encarecidamente algunas alternativas que no requieran la instalación de Office y la ejecución del servidor, y que puedan realizar tareas comunes de forma más eficaz y rápida que la automatización en esta configuración. Antes de involucrar a Office como componente del lado servidor en el proyecto, tenga en cuenta las alternativas.

### <a name="microsoft-graph"></a>Microsoft Graph

La API de Microsoft Graph proporciona acceso a los servicios, datos e inteligencia que están disponibles para los usuarios y las soluciones como parte de Microsoft Cloud, incluidos muchos servicios que admiten las necesidades de la automatización desatendida: acceso al correo/calendario/contactos/archivos de los usuarios, la conversión de documentos, el cálculo de libros de Excel y mucho más. Estos servicios están diseñados para uso desatendido y acceso a gran escala, y usan una sintaxis de API RESTful estándar. Para obtener más información sobre Microsoft Graph y cómo usarla para trabajar con los datos de los usuarios, visite el siguiente ejemplo:

- [Información general de Microsoft Graph](https://docs.microsoft.com/graph/overview) 
- [Introducción a Microsoft Graph](https://developer.microsoft.com/graph/get-started)
- [Descargar un archivo en otro formato](https://docs.microsoft.com/graph/api/driveitem-get-content-format?view=graph-rest-1.0&tabs=http) (conversión de archivos)
- [Trabajar con Excel en Microsoft Graph](https://docs.microsoft.com/graph/api/resources/excel?view=graph-rest-1.0) (detalles del libro)

### <a name="open-xml-file-formats"></a>Formatos de archivo Open XML

Muchas tareas de automatización implican la creación o edición de documentos. Office admite formatos de archivo Open XML que permiten a los desarrolladores crear, editar, leer y transformar contenido de archivos con tecnologías estándar de XML y ZIP, definidas en el estándar internacional ISO 29500. Estos formatos de archivo pueden manipularse a través de cualquier herramienta ZIP/XML, incluido el espacio de nombres System.IO.Package.IO en Microsoft .NET 3. x Framework. La edición directa de los formatos de archivo es el método recomendado y compatible para controlar los cambios en los archivos de Office desde un servicio.

Microsoft proporciona un SDK para manipular formatos de archivo Open XML desde .NET 3. x Framework. Para obtener más información sobre el SDK y cómo usar el SDK para crear o editar archivos Open XML, visite el siguiente ejemplo:

- [Descripción de los formatos de archivo Open XML](https://docs.microsoft.com/office/open-xml/understanding-the-open-xml-file-formats)
- [Bienvenido al SDK de Open XML 2,5 para Office](https://docs.microsoft.com/office/open-xml/open-xml-sdk)
