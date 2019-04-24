---
title: Sección archivo de configuración de formulario [Descripción]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ce91a65-17db-4ee2-ad59-01fd5b1f1ea7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ddc59d6c503d44a0575679fce694cc34499d8e2a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320989"
---
# <a name="form-configuration-file-description-section"></a>Sección archivo de configuración de formulario [Descripción]
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La sección **[Description]** enumera todas las propiedades del formulario que están asociadas a controles en la interfaz de usuario del formulario, además de los atributos que se usan para buscar el formulario. Las entradas **MessageClass**, **CLSID**y **displayName** , que identifican el nombre de la clase de mensaje del formulario, su GUID y el nombre para mostrar de la clase de mensaje, respectivamente, son entradas necesarias que se usan para ubicar el formulario en la biblioteca de formularios. . Las entradas restantes son opcionales. El formato de la sección **[Descripción]** es: 
  
La sección **[Description]** enumera todas las propiedades del formulario que están asociadas a controles en la interfaz de usuario del formulario, además de los atributos que se usan para buscar el formulario. Las entradas **MessageClass**, **CLSID**y **displayName** , que identifican el nombre de la clase de mensaje del formulario, su GUID y el nombre para mostrar de la clase de mensaje, respectivamente, son entradas necesarias que se usan para ubicar el formulario en la biblioteca de formularios. . Las entradas restantes son opcionales. El formato de la sección **[Descripción]** es: 
  
 **Descriptiva MessageClass** =  (_cadena_ )
  
 **** =  _GUID_ de CLSID
  
 **DisplayName** =  _displayedstring_
  
 **** =  _Ruta_ de SmallIcon
  
 **LargeIcon** =  _ruta de acceso_
  
Las entradas opcionales son:
  
 **** =  _Cadena mostrada_ en la categoría
  
 **** =  _Cadena mostrada_ en la subcategoría
  
 **** =  _Cadena mostrada_ como comentario
  
 **** =  _Cadena mostrada_ por el propietario
  
 **Número** =  de cadena que se_muestra_
  
 **** =  _Número entero_ de versión
  
 **Cadena de configuración regional**__  =  
  
 **** =  _Entero_ oculto
  
 **** =  _Cadena_ DesignerToolName
  
 **** =  _CLSID_ DesignerToolGuid
  
 **** =  _CLSID_ DesignerRuntimeGuid
  
 **ComposeInFolder** =  _0 | 1_
  
 **** =  _Cadena_ ComposeCommand
  
Los instaladores de formularios usan las entradas de **categoría** y **Subcategoría** para configurar la categorización predeterminada de los formularios en la interfaz de usuario de la aplicación de cliente. Por ejemplo, una jerarquía se puede configurar donde "servicio de asistencia" es la categoría y "software" y "hardware" son las subcategorías. Las aplicaciones de visor pueden usar esta categorización para mostrar los mensajes de forma más organizada. Las entradas **Comentario**, **propietario**y **número** son todas las cadenas de comentarios que aparecen en la interfaz de usuario de la aplicación cliente. Estas propiedades son específicas del formulario que se pueden usar a discreción del desarrollador del formulario. Por ejemplo, la entrada de **Comentario** puede usarse para indicar el propósito del formulario, la entrada de **propietario** usada para indicar la persona u organización responsable de mantener el formulario, y el número que se usa para realizar un seguimiento de la versión diferente del formulario. Para la entrada de **Comentario** , se pueden incluir hasta diez líneas de comentarios. La primera línea de comentarios usa la palabra "comentario" como la clave, la segunda línea de comentarios usa "Comment1" como clave, y así sucesivamente mediante "Comment9". 
  
Las entradas **LargeIcon** y **SmallIcon** se usan para especificar la ruta de acceso de los recursos de iconos usados para mostrar iconos en la interfaz de usuario de la aplicación cliente, normalmente es para las filas de tabla que incluyen el **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) columnas de propiedad o **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)). Los nombres de archivo de icono pueden especificarse como rutas de directorios relativas al directorio en el que está instalado el archivo de configuración de formulario. La entrada **version** se usa para indicar el número de versión del formulario. **Locale** es el identificador de idioma de tres letras de la biblioteca de formularios de destino. Puede encontrar una lista de estos identificadores en la _Referencia del programador de Win32_.
  
La entrada **oculta** indica si el formulario debe mostrarse en la interfaz de usuario del proveedor de la biblioteca de formularios: 1 indica que el archivo está oculto y 0 indica que el formulario está visible. A continuación se muestra un archivo de configuración de formulario de ejemplo. 
  
La entrada **ComposeInFolder** controla si el formulario está diseñado para colocarse en la carpeta actual o en la bandeja de entrada del usuario cuando el usuario guarda el mensaje mientras lo redacta: 1 indica que el formulario debe ir en la carpeta actual y 0 indica que debe ir a la bandeja de entrada. 
  
La entrada **ComposeCommand** es la cadena que se va a colocar en el menú de redacción de la aplicación cliente. Si no se especifica, se usará la entrada **displayName** . 
  
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


