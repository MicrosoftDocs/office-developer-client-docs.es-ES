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
# <a name="form-configuration-file-description-section"></a><span data-ttu-id="eeb62-103">Sección archivo de configuración de formulario [Descripción]</span><span class="sxs-lookup"><span data-stu-id="eeb62-103">Form Configuration File [Description] Section</span></span>
 
<span data-ttu-id="eeb62-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eeb62-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eeb62-105">La sección **[Description]** enumera todas las propiedades del formulario que están asociadas a controles en la interfaz de usuario del formulario, además de los atributos que se usan para buscar el formulario.</span><span class="sxs-lookup"><span data-stu-id="eeb62-105">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="eeb62-106">Las entradas **MessageClass**, **CLSID**y **displayName** , que identifican el nombre de la clase de mensaje del formulario, su GUID y el nombre para mostrar de la clase de mensaje, respectivamente, son entradas necesarias que se usan para ubicar el formulario en la biblioteca de formularios. .</span><span class="sxs-lookup"><span data-stu-id="eeb62-106">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="eeb62-107">Las entradas restantes son opcionales.</span><span class="sxs-lookup"><span data-stu-id="eeb62-107">The remaining entries are optional.</span></span> <span data-ttu-id="eeb62-108">El formato de la sección **[Descripción]** es:</span><span class="sxs-lookup"><span data-stu-id="eeb62-108">The format of the **[Description]** section is:</span></span> 
  
<span data-ttu-id="eeb62-109">La sección **[Description]** enumera todas las propiedades del formulario que están asociadas a controles en la interfaz de usuario del formulario, además de los atributos que se usan para buscar el formulario.</span><span class="sxs-lookup"><span data-stu-id="eeb62-109">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="eeb62-110">Las entradas **MessageClass**, **CLSID**y **displayName** , que identifican el nombre de la clase de mensaje del formulario, su GUID y el nombre para mostrar de la clase de mensaje, respectivamente, son entradas necesarias que se usan para ubicar el formulario en la biblioteca de formularios. .</span><span class="sxs-lookup"><span data-stu-id="eeb62-110">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="eeb62-111">Las entradas restantes son opcionales.</span><span class="sxs-lookup"><span data-stu-id="eeb62-111">The remaining entries are optional.</span></span> <span data-ttu-id="eeb62-112">El formato de la sección **[Descripción]** es:</span><span class="sxs-lookup"><span data-stu-id="eeb62-112">The format of the **[Description]** section is:</span></span> 
  
 <span data-ttu-id="eeb62-113">**Descriptiva MessageClass** =  (_cadena_ )</span><span class="sxs-lookup"><span data-stu-id="eeb62-113">**[Description] MessageClass** =  _string_</span></span>
  
 <span data-ttu-id="eeb62-114">\*\*\*\* =  _GUID_ de CLSID</span><span class="sxs-lookup"><span data-stu-id="eeb62-114">**Clsid** =  _guid_</span></span>
  
 <span data-ttu-id="eeb62-115">**DisplayName** =  _displayedstring_</span><span class="sxs-lookup"><span data-stu-id="eeb62-115">**DisplayName** =  _displayedstring_</span></span>
  
 <span data-ttu-id="eeb62-116">\*\*\*\* =  _Ruta_ de SmallIcon</span><span class="sxs-lookup"><span data-stu-id="eeb62-116">**SmallIcon** =  _path_</span></span>
  
 <span data-ttu-id="eeb62-117">**LargeIcon** =  _ruta de acceso_</span><span class="sxs-lookup"><span data-stu-id="eeb62-117">**LargeIcon** =  _path_</span></span>
  
<span data-ttu-id="eeb62-118">Las entradas opcionales son:</span><span class="sxs-lookup"><span data-stu-id="eeb62-118">Optional entries are:</span></span>
  
 <span data-ttu-id="eeb62-119">\*\*\*\* =  _Cadena mostrada_ en la categoría</span><span class="sxs-lookup"><span data-stu-id="eeb62-119">**Category** =  _displayed string_</span></span>
  
 <span data-ttu-id="eeb62-120">\*\*\*\* =  _Cadena mostrada_ en la subcategoría</span><span class="sxs-lookup"><span data-stu-id="eeb62-120">**Subcategory** =  _displayed string_</span></span>
  
 <span data-ttu-id="eeb62-121">\*\*\*\* =  _Cadena mostrada_ como comentario</span><span class="sxs-lookup"><span data-stu-id="eeb62-121">**Comment** =  _displayed string_</span></span>
  
 <span data-ttu-id="eeb62-122">\*\*\*\* =  _Cadena mostrada_ por el propietario</span><span class="sxs-lookup"><span data-stu-id="eeb62-122">**Owner** =  _displayed string_</span></span>
  
 <span data-ttu-id="eeb62-123">**Número** =  de cadena que se_muestra_</span><span class="sxs-lookup"><span data-stu-id="eeb62-123">**Number** =  _displayed string_</span></span>
  
 <span data-ttu-id="eeb62-124">\*\*\*\* =  _Número entero_ de versión</span><span class="sxs-lookup"><span data-stu-id="eeb62-124">**Version** =  _integer_</span></span>
  
 <span data-ttu-id="eeb62-125">**Cadena de configuración regional**__  =  </span><span class="sxs-lookup"><span data-stu-id="eeb62-125">**Locale** =  _string_</span></span>
  
 <span data-ttu-id="eeb62-126">\*\*\*\* =  _Entero_ oculto</span><span class="sxs-lookup"><span data-stu-id="eeb62-126">**Hidden** =  _integer_</span></span>
  
 <span data-ttu-id="eeb62-127">\*\*\*\* =  _Cadena_ DesignerToolName</span><span class="sxs-lookup"><span data-stu-id="eeb62-127">**DesignerToolName** =  _string_</span></span>
  
 <span data-ttu-id="eeb62-128">\*\*\*\* =  _CLSID_ DesignerToolGuid</span><span class="sxs-lookup"><span data-stu-id="eeb62-128">**DesignerToolGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="eeb62-129">\*\*\*\* =  _CLSID_ DesignerRuntimeGuid</span><span class="sxs-lookup"><span data-stu-id="eeb62-129">**DesignerRuntimeGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="eeb62-130">**ComposeInFolder** =  _0 | 1_</span><span class="sxs-lookup"><span data-stu-id="eeb62-130">**ComposeInFolder** =  _0|1_</span></span>
  
 <span data-ttu-id="eeb62-131">\*\*\*\* =  _Cadena_ ComposeCommand</span><span class="sxs-lookup"><span data-stu-id="eeb62-131">**ComposeCommand** =  _string_</span></span>
  
<span data-ttu-id="eeb62-132">Los instaladores de formularios usan las entradas de **categoría** y **Subcategoría** para configurar la categorización predeterminada de los formularios en la interfaz de usuario de la aplicación de cliente.</span><span class="sxs-lookup"><span data-stu-id="eeb62-132">The **Category** and **Subcategory** entries are used by form installers to set up the default categorization of forms within client application's user interface.</span></span> <span data-ttu-id="eeb62-133">Por ejemplo, una jerarquía se puede configurar donde "servicio de asistencia" es la categoría y "software" y "hardware" son las subcategorías.</span><span class="sxs-lookup"><span data-stu-id="eeb62-133">For example a hierarchy could be set up where "Help Desk" is the category and "Software" and "Hardware" were the subcategories.</span></span> <span data-ttu-id="eeb62-134">Las aplicaciones de visor pueden usar esta categorización para mostrar los mensajes de forma más organizada.</span><span class="sxs-lookup"><span data-stu-id="eeb62-134">This categorization can then be used by viewer applications to display messages in a more organized way.</span></span> <span data-ttu-id="eeb62-135">Las entradas **Comentario**, **propietario**y **número** son todas las cadenas de comentarios que aparecen en la interfaz de usuario de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="eeb62-135">The **Comment**, **Owner**, and **Number** entries are all comment strings that appear in client application's user interface.</span></span> <span data-ttu-id="eeb62-136">Estas propiedades son específicas del formulario que se pueden usar a discreción del desarrollador del formulario.</span><span class="sxs-lookup"><span data-stu-id="eeb62-136">These are form specific properties that can be used at the discretion of the form developer.</span></span> <span data-ttu-id="eeb62-137">Por ejemplo, la entrada de **Comentario** puede usarse para indicar el propósito del formulario, la entrada de **propietario** usada para indicar la persona u organización responsable de mantener el formulario, y el número que se usa para realizar un seguimiento de la versión diferente del formulario.</span><span class="sxs-lookup"><span data-stu-id="eeb62-137">For example, the **Comment** entry can be used to indicate the purpose of the form, the **Owner** entry used to indicate the person or organization responsible for maintaining the form, and the number used to track different version of the form.</span></span> <span data-ttu-id="eeb62-138">Para la entrada de **Comentario** , se pueden incluir hasta diez líneas de comentarios.</span><span class="sxs-lookup"><span data-stu-id="eeb62-138">For the **Comment** entry, up to ten lines of comments can be included.</span></span> <span data-ttu-id="eeb62-139">La primera línea de comentarios usa la palabra "comentario" como la clave, la segunda línea de comentarios usa "Comment1" como clave, y así sucesivamente mediante "Comment9".</span><span class="sxs-lookup"><span data-stu-id="eeb62-139">The first line of comments uses the word "Comment" as the key, the second line of comments uses "Comment1" as the key, and so on through "Comment9."</span></span> 
  
<span data-ttu-id="eeb62-140">Las entradas **LargeIcon** y **SmallIcon** se usan para especificar la ruta de acceso de los recursos de iconos usados para mostrar iconos en la interfaz de usuario de la aplicación cliente, normalmente es para las filas de tabla que incluyen el **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) columnas de propiedad o **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="eeb62-140">The **LargeIcon** and **SmallIcon** entries are used to specify the path for the icon resources used to display icons in the client application's user interface, typically this is for table rows that include the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property columns.</span></span> <span data-ttu-id="eeb62-141">Los nombres de archivo de icono pueden especificarse como rutas de directorios relativas al directorio en el que está instalado el archivo de configuración de formulario.</span><span class="sxs-lookup"><span data-stu-id="eeb62-141">Icon file names can be specified as pathnames relative to the directory where the form configuration file is installed.</span></span> <span data-ttu-id="eeb62-142">La entrada **version** se usa para indicar el número de versión del formulario.</span><span class="sxs-lookup"><span data-stu-id="eeb62-142">The **Version** entry is used to indicate the version number of the form.</span></span> <span data-ttu-id="eeb62-143">**Locale** es el identificador de idioma de tres letras de la biblioteca de formularios de destino.</span><span class="sxs-lookup"><span data-stu-id="eeb62-143">**Locale** is the three-letter language identifier of the destination form library.</span></span> <span data-ttu-id="eeb62-144">Puede encontrar una lista de estos identificadores en la _Referencia del programador de Win32_.</span><span class="sxs-lookup"><span data-stu-id="eeb62-144">A list of these identifiers can be found in the  _Win32 Programmer's Reference_.</span></span>
  
<span data-ttu-id="eeb62-145">La entrada **oculta** indica si el formulario debe mostrarse en la interfaz de usuario del proveedor de la biblioteca de formularios: 1 indica que el archivo está oculto y 0 indica que el formulario está visible.</span><span class="sxs-lookup"><span data-stu-id="eeb62-145">The **Hidden** entry indicates whether the form should be displayed in a form library provider's user interface: 1 indicates that the file is hidden and 0 indicates that the form is visible.</span></span> <span data-ttu-id="eeb62-146">A continuación se muestra un archivo de configuración de formulario de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="eeb62-146">An example form configuration file is shown following.</span></span> 
  
<span data-ttu-id="eeb62-147">La entrada **ComposeInFolder** controla si el formulario está diseñado para colocarse en la carpeta actual o en la bandeja de entrada del usuario cuando el usuario guarda el mensaje mientras lo redacta: 1 indica que el formulario debe ir en la carpeta actual y 0 indica que debe ir a la bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="eeb62-147">The **ComposeInFolder** entry controls whether the form is designed to be placed in the current folder or in the user's Inbox when the user saves the message while composing it: 1 indicates that the form should go in the current folder and 0 indicates that it should go in the Inbox.</span></span> 
  
<span data-ttu-id="eeb62-148">La entrada **ComposeCommand** es la cadena que se va a colocar en el menú de redacción de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="eeb62-148">The **ComposeCommand** entry is the string to be placed in the client application's compose menu.</span></span> <span data-ttu-id="eeb62-149">Si no se especifica, se usará la entrada **displayName** .</span><span class="sxs-lookup"><span data-stu-id="eeb62-149">If this is not specified, the **DisplayName** entry will be used.</span></span> 
  
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


