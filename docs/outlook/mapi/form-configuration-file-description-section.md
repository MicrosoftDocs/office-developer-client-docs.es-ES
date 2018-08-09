---
title: Sección del archivo de configuración de formulario [Descripción]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ce91a65-17db-4ee2-ad59-01fd5b1f1ea7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d3673c3b10afb55121339e335163ce9b2e5937e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816840"
---
# <a name="form-configuration-file-description-section"></a>Sección del archivo de configuración de formulario [Descripción]
 
**Hace referencia a**: Outlook 
  
La sección **[descripción]** enumera todas las propiedades del formulario que están asociadas con los controles en el formulario de la interfaz de usuario, además de atributos que se usan para localizar el formulario. El **MessageClass**, **Clsid**y entradas de **DisplayName** , que identifican el nombre de clase de mensaje del formulario, su GUID y nombre para mostrar de la clase de mensaje, respectivamente, son entradas necesarias que se usa para buscar el formulario en la biblioteca de formularios . Las entradas restantes son opcionales. El formato de la sección **[descripción]** es: 
  
La sección **[descripción]** enumera todas las propiedades del formulario que están asociadas con los controles en el formulario de la interfaz de usuario, además de atributos que se usan para localizar el formulario. El **MessageClass**, **Clsid**y entradas de **DisplayName** , que identifican el nombre de clase de mensaje del formulario, su GUID y nombre para mostrar de la clase de mensaje, respectivamente, son entradas necesarias que se usa para buscar el formulario en la biblioteca de formularios . Las entradas restantes son opcionales. El formato de la sección **[descripción]** es: 
  
 **[Descripción] MessageClass** =  _cadena_
  
 **CLSID** =  _guid_
  
 **DisplayName** =  _displayedstring_
  
 **SmallIcon** =  _ruta de acceso_
  
 **LargeIcon** =  _ruta de acceso_
  
Entradas opcionales son:
  
 **Categoría** =  _muestra la cadena_
  
 **Subcategoría** =  _muestra la cadena_
  
 **Comentario** =  _muestra la cadena_
  
 **Propietario** =  _muestra la cadena_
  
 **Número de** =  _muestra la cadena_
  
 **Versión** =  _entero_
  
 **Configuración regional** =  _cadena_
  
 **Oculto** =  _entero_
  
 **DesignerToolName** =  _cadena_
  
 **DesignerToolGuid** =  _clsid_
  
 **DesignerRuntimeGuid** =  _clsid_
  
 **ComposeInFolder** =  _0 | 1_
  
 **ComposeCommand** =  _cadena_
  
Se utilizan las entradas de la **categoría** y **subcategoría** por instaladores del formulario para configurar la categorización de forma predeterminada de los formularios dentro de la interfaz de usuario de la aplicación cliente. Por ejemplo, se puede establecer una jerarquía donde "Help Desk" es la categoría y "Software" y "Hardware" eran las subcategorías. Este categorización, a continuación, se puede usar mediante aplicaciones de visor para mostrar los mensajes de una forma más organizada. Las entradas de **comentario**, el **propietario**y el **número** están todas las cadenas de comentario que aparecen en la interfaz de usuario de la aplicación cliente. Estos son propiedades específicas del formulario que se pueden usar en función del criterio del desarrollador de formulario. Por ejemplo, la entrada de **comentario** puede utilizarse para indicar el propósito del formulario, la entrada de **propietario** que se utiliza para indicar la persona u organización responsable de mantener el formulario y el número que se usa para realizar un seguimiento de una versión diferente del formulario. El **comentario** se puede incluir entrada hasta diez líneas de comentarios. La primera línea de comentarios de la palabra "Comentario" como la clave, la segunda línea de comentarios utiliza "Comentario1" como la clave, y así sucesivamente a través de "Comment9". 
  
Las entradas **incluidas** y **SmallIcon** se utilizan para especificar la ruta de acceso para los recursos de icono que se usa para mostrar iconos en la interfaz de usuario de la aplicación cliente, normalmente se trata de las filas de tabla que incluyen la **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) o las columnas de propiedad de **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)). Los nombres de archivo de icono pueden especificarse como rutas de acceso relativas al directorio donde está instalado el archivo de configuración del formulario. La entrada de la **versión** se usa para indicar el número de versión del formulario. **Configuración regional** es el identificador de idioma de tres letras de la biblioteca de formulario de destino. Una lista de estos identificadores puede encontrarse en la _referencia del programador de Win32_.
  
La entrada **oculto** indica si se debe mostrar el formulario en la interfaz de usuario del proveedor de biblioteca de formulario: 1 indica que el archivo está oculto y 0 indica que el formulario está visible. Se muestra un archivo de configuración del formulario de ejemplo siguiente. 
  
La entrada **ComposeInFolder** controla si el formulario está diseñado para colocarse en la carpeta actual o en la Bandeja de entrada del usuario cuando el usuario guarda el mensaje mientras se redacta: 1 indica que el formulario debe ir en la carpeta actual y 0 indica que debe vaya en la Bandeja de entrada. 
  
La entrada **ComposeCommand** es la cadena que se sitúa en la aplicación cliente del menú de redacción. Si no se especifica, se usará la entrada **DisplayName** . 
  
```cpp
[Description]
MessageClass = IPM.Help
Clsid = {00020D31-0000-0000-C000-000000000046}
DisplayName = Help Desk Request Form
;optional entries
Category = Help Desk Requests
Subcategory = New Requests
Comment = Use this form to request network assistance
Owner = Help Desk
Number = 1
SmallIcon = C:\WINDOWS|EFORMS\HELPDESK\HDSMALL.ICO
LargeIcon = C:\WINDOWS|EFORMS\HELPDESK\HDLARGE.ICO
Version = 1.00
Locale = enu
Hidden = 0
ComposeInFolder = 0
ComposeCommand = &Help Desk Request
 
```


