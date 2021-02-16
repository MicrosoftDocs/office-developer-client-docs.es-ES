---
title: Sección Archivo de configuración de formulario [Descripción]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ce91a65-17db-4ee2-ad59-01fd5b1f1ea7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ddc59d6c503d44a0575679fce694cc34499d8e2a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433097"
---
# <a name="form-configuration-file-description-section"></a>Sección Archivo de configuración de formulario [Descripción]
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La **sección [Descripción]** enumera todas las propiedades del formulario que están asociadas a controles en la interfaz de usuario del formulario, además de los atributos que se usan para buscar el formulario. Las **entradas MessageClass**, **Clsid** y **DisplayName,** que identifican el nombre de la clase de mensaje del formulario, su GUID y el nombre para mostrar de la clase de mensaje, respectivamente, son entradas necesarias que se usan para localizar el formulario dentro de la biblioteca de formularios. Las entradas restantes son opcionales. El formato de la **sección [Descripción]** es: 
  
La **sección [Descripción]** enumera todas las propiedades del formulario que están asociadas a controles en la interfaz de usuario del formulario, además de los atributos que se usan para buscar el formulario. Las **entradas MessageClass**, **Clsid** y **DisplayName,** que identifican el nombre de la clase de mensaje del formulario, su GUID y el nombre para mostrar de la clase de mensaje, respectivamente, son entradas necesarias que se usan para localizar el formulario dentro de la biblioteca de formularios. Las entradas restantes son opcionales. El formato de la **sección [Descripción]** es: 
  
 **[Descripción] MessageClass**  =   _string_
  
 **Clsid**  =   _guid_
  
 **DisplayName**  =   _displayedstring_
  
 **SmallIcon**  =   _ruta de acceso_
  
 **LargeIcon**  =   _ruta de acceso_
  
Las entradas opcionales son:
  
 **Categoría**  =   _cadena mostrada_
  
 **Subcategoría**  =   _cadena mostrada_
  
 **Comentario**  =   _cadena mostrada_
  
 **Propietario**  =   _cadena mostrada_
  
 **Número**  =   _cadena mostrada_
  
 **Versión**  =   _integer_
  
 **Configuración regional**  =   _string_
  
 **Oculto**  =   _integer_
  
 **DesignerToolName**  =   _string_
  
 **DesignerToolGuid**  =   _clsid_
  
 **DesignerRuntimeGuid**  =   _clsid_
  
 **ComposeInFolder**  =   _0|1_
  
 **ComposeCommand**  =   _string_
  
Los **instaladores** de formularios usan las entradas Category y **Subcategory** para configurar la categorización predeterminada de los formularios en la interfaz de usuario de la aplicación cliente. Por ejemplo, se podría configurar una jerarquía donde "Help Desk" es la categoría y "Software" y "Hardware" eran las subcategorías. A continuación, las aplicaciones de visor pueden usar esta categorización para mostrar los mensajes de una forma más organizada. Las **entradas Comment**, **Owner** y **Number** son todas las cadenas de comentarios que aparecen en la interfaz de usuario de la aplicación cliente. Se trata de propiedades específicas de formulario que se pueden usar a discreción del desarrollador del formulario. Por ejemplo,  la entrada Comment puede usarse para indicar la finalidad del formulario, la entrada **Owner** usada para indicar la persona u organización responsable de mantener el formulario y el número usado para realizar un seguimiento de una versión diferente del formulario. Para la **entrada Comentario,** se pueden incluir hasta diez líneas de comentarios. La primera línea de comentarios usa la palabra "Comentario" como clave, la segunda línea de comentarios usa "Comentario1" como clave, y así sucesivamente a través de "Comentario9". 
  
Las entradas **LargeIcon** y **SmallIcon** se usan para especificar la ruta de acceso de los recursos de icono usados para mostrar iconos en la interfaz de usuario de la aplicación cliente, normalmente es para las filas de tabla que incluyen las columnas de la propiedad **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) o **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)). Los nombres de archivo de icono se pueden especificar como nombres de ruta de acceso en relación con el directorio donde está instalado el archivo de configuración del formulario. La **entrada** Version se usa para indicar el número de versión del formulario. **La configuración regional** es el identificador de idioma de tres letras de la biblioteca de formularios de destino. Puedes encontrar una lista de estos identificadores en la Referencia del programador _de Win32._
  
La **entrada** Oculta indica si el formulario debe mostrarse en la interfaz de usuario de un proveedor de bibliotecas de formularios: 1 indica que el archivo está oculto y 0 indica que el formulario está visible. A continuación se muestra un archivo de configuración de formulario de ejemplo. 
  
La entrada **ComposeInFolder** controla si el formulario está diseñado para colocarse en la carpeta actual o en la Bandeja de entrada del usuario cuando el usuario guarda el mensaje mientras lo redacta: 1 indica que el formulario debe ir en la carpeta actual y 0 indica que debe ir en la Bandeja de entrada. 
  
La **entrada ComposeCommand** es la cadena que se colocará en el menú de redacción de la aplicación cliente. Si no se especifica, se usará **la entrada DisplayName.** 
  
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


