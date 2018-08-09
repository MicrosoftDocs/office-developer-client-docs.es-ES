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
# <a name="form-configuration-file-description-section"></a><span data-ttu-id="eec34-103">Sección del archivo de configuración de formulario [Descripción]</span><span class="sxs-lookup"><span data-stu-id="eec34-103">Form Configuration File [Description] Section</span></span>
 
<span data-ttu-id="eec34-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="eec34-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="eec34-105">La sección **[descripción]** enumera todas las propiedades del formulario que están asociadas con los controles en el formulario de la interfaz de usuario, además de atributos que se usan para localizar el formulario.</span><span class="sxs-lookup"><span data-stu-id="eec34-105">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="eec34-106">El **MessageClass**, **Clsid**y entradas de **DisplayName** , que identifican el nombre de clase de mensaje del formulario, su GUID y nombre para mostrar de la clase de mensaje, respectivamente, son entradas necesarias que se usa para buscar el formulario en la biblioteca de formularios .</span><span class="sxs-lookup"><span data-stu-id="eec34-106">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="eec34-107">Las entradas restantes son opcionales.</span><span class="sxs-lookup"><span data-stu-id="eec34-107">The remaining entries are optional.</span></span> <span data-ttu-id="eec34-108">El formato de la sección **[descripción]** es:</span><span class="sxs-lookup"><span data-stu-id="eec34-108">The format of the **[Description]** section is:</span></span> 
  
<span data-ttu-id="eec34-109">La sección **[descripción]** enumera todas las propiedades del formulario que están asociadas con los controles en el formulario de la interfaz de usuario, además de atributos que se usan para localizar el formulario.</span><span class="sxs-lookup"><span data-stu-id="eec34-109">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="eec34-110">El **MessageClass**, **Clsid**y entradas de **DisplayName** , que identifican el nombre de clase de mensaje del formulario, su GUID y nombre para mostrar de la clase de mensaje, respectivamente, son entradas necesarias que se usa para buscar el formulario en la biblioteca de formularios .</span><span class="sxs-lookup"><span data-stu-id="eec34-110">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="eec34-111">Las entradas restantes son opcionales.</span><span class="sxs-lookup"><span data-stu-id="eec34-111">The remaining entries are optional.</span></span> <span data-ttu-id="eec34-112">El formato de la sección **[descripción]** es:</span><span class="sxs-lookup"><span data-stu-id="eec34-112">The format of the **[Description]** section is:</span></span> 
  
 <span data-ttu-id="eec34-113">**[Descripción] MessageClass** =  _cadena_</span><span class="sxs-lookup"><span data-stu-id="eec34-113">**[Description] MessageClass** =  _string_</span></span>
  
 <span data-ttu-id="eec34-114">**CLSID** =  _guid_</span><span class="sxs-lookup"><span data-stu-id="eec34-114">**Clsid** =  _guid_</span></span>
  
 <span data-ttu-id="eec34-115">**DisplayName** =  _displayedstring_</span><span class="sxs-lookup"><span data-stu-id="eec34-115">**DisplayName** =  _displayedstring_</span></span>
  
 <span data-ttu-id="eec34-116">**SmallIcon** =  _ruta de acceso_</span><span class="sxs-lookup"><span data-stu-id="eec34-116">**SmallIcon** =  _path_</span></span>
  
 <span data-ttu-id="eec34-117">**LargeIcon** =  _ruta de acceso_</span><span class="sxs-lookup"><span data-stu-id="eec34-117">**LargeIcon** =  _path_</span></span>
  
<span data-ttu-id="eec34-118">Entradas opcionales son:</span><span class="sxs-lookup"><span data-stu-id="eec34-118">Optional entries are:</span></span>
  
 <span data-ttu-id="eec34-119">**Categoría** =  _muestra la cadena_</span><span class="sxs-lookup"><span data-stu-id="eec34-119">**Category** =  _displayed string_</span></span>
  
 <span data-ttu-id="eec34-120">**Subcategoría** =  _muestra la cadena_</span><span class="sxs-lookup"><span data-stu-id="eec34-120">**Subcategory** =  _displayed string_</span></span>
  
 <span data-ttu-id="eec34-121">**Comentario** =  _muestra la cadena_</span><span class="sxs-lookup"><span data-stu-id="eec34-121">**Comment** =  _displayed string_</span></span>
  
 <span data-ttu-id="eec34-122">**Propietario** =  _muestra la cadena_</span><span class="sxs-lookup"><span data-stu-id="eec34-122">**Owner** =  _displayed string_</span></span>
  
 <span data-ttu-id="eec34-123">**Número de** =  _muestra la cadena_</span><span class="sxs-lookup"><span data-stu-id="eec34-123">**Number** =  _displayed string_</span></span>
  
 <span data-ttu-id="eec34-124">**Versión** =  _entero_</span><span class="sxs-lookup"><span data-stu-id="eec34-124">**Version** =  _integer_</span></span>
  
 <span data-ttu-id="eec34-125">**Configuración regional** =  _cadena_</span><span class="sxs-lookup"><span data-stu-id="eec34-125">**Locale** =  _string_</span></span>
  
 <span data-ttu-id="eec34-126">**Oculto** =  _entero_</span><span class="sxs-lookup"><span data-stu-id="eec34-126">**Hidden** =  _integer_</span></span>
  
 <span data-ttu-id="eec34-127">**DesignerToolName** =  _cadena_</span><span class="sxs-lookup"><span data-stu-id="eec34-127">**DesignerToolName** =  _string_</span></span>
  
 <span data-ttu-id="eec34-128">**DesignerToolGuid** =  _clsid_</span><span class="sxs-lookup"><span data-stu-id="eec34-128">**DesignerToolGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="eec34-129">**DesignerRuntimeGuid** =  _clsid_</span><span class="sxs-lookup"><span data-stu-id="eec34-129">**DesignerRuntimeGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="eec34-130">**ComposeInFolder** =  _0 | 1_</span><span class="sxs-lookup"><span data-stu-id="eec34-130">**ComposeInFolder** =  _0|1_</span></span>
  
 <span data-ttu-id="eec34-131">**ComposeCommand** =  _cadena_</span><span class="sxs-lookup"><span data-stu-id="eec34-131">**ComposeCommand** =  _string_</span></span>
  
<span data-ttu-id="eec34-132">Se utilizan las entradas de la **categoría** y **subcategoría** por instaladores del formulario para configurar la categorización de forma predeterminada de los formularios dentro de la interfaz de usuario de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="eec34-132">The **Category** and **Subcategory** entries are used by form installers to set up the default categorization of forms within client application's user interface.</span></span> <span data-ttu-id="eec34-133">Por ejemplo, se puede establecer una jerarquía donde "Help Desk" es la categoría y "Software" y "Hardware" eran las subcategorías.</span><span class="sxs-lookup"><span data-stu-id="eec34-133">For example a hierarchy could be set up where "Help Desk" is the category and "Software" and "Hardware" were the subcategories.</span></span> <span data-ttu-id="eec34-134">Este categorización, a continuación, se puede usar mediante aplicaciones de visor para mostrar los mensajes de una forma más organizada.</span><span class="sxs-lookup"><span data-stu-id="eec34-134">This categorization can then be used by viewer applications to display messages in a more organized way.</span></span> <span data-ttu-id="eec34-135">Las entradas de **comentario**, el **propietario**y el **número** están todas las cadenas de comentario que aparecen en la interfaz de usuario de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="eec34-135">The **Comment**, **Owner**, and **Number** entries are all comment strings that appear in client application's user interface.</span></span> <span data-ttu-id="eec34-136">Estos son propiedades específicas del formulario que se pueden usar en función del criterio del desarrollador de formulario.</span><span class="sxs-lookup"><span data-stu-id="eec34-136">These are form specific properties that can be used at the discretion of the form developer.</span></span> <span data-ttu-id="eec34-137">Por ejemplo, la entrada de **comentario** puede utilizarse para indicar el propósito del formulario, la entrada de **propietario** que se utiliza para indicar la persona u organización responsable de mantener el formulario y el número que se usa para realizar un seguimiento de una versión diferente del formulario.</span><span class="sxs-lookup"><span data-stu-id="eec34-137">For example, the **Comment** entry can be used to indicate the purpose of the form, the **Owner** entry used to indicate the person or organization responsible for maintaining the form, and the number used to track different version of the form.</span></span> <span data-ttu-id="eec34-138">El **comentario** se puede incluir entrada hasta diez líneas de comentarios.</span><span class="sxs-lookup"><span data-stu-id="eec34-138">For the **Comment** entry, up to ten lines of comments can be included.</span></span> <span data-ttu-id="eec34-139">La primera línea de comentarios de la palabra "Comentario" como la clave, la segunda línea de comentarios utiliza "Comentario1" como la clave, y así sucesivamente a través de "Comment9".</span><span class="sxs-lookup"><span data-stu-id="eec34-139">The first line of comments uses the word "Comment" as the key, the second line of comments uses "Comment1" as the key, and so on through "Comment9."</span></span> 
  
<span data-ttu-id="eec34-140">Las entradas **incluidas** y **SmallIcon** se utilizan para especificar la ruta de acceso para los recursos de icono que se usa para mostrar iconos en la interfaz de usuario de la aplicación cliente, normalmente se trata de las filas de tabla que incluyen la **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) o las columnas de propiedad de **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="eec34-140">The **LargeIcon** and **SmallIcon** entries are used to specify the path for the icon resources used to display icons in the client application's user interface, typically this is for table rows that include the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property columns.</span></span> <span data-ttu-id="eec34-141">Los nombres de archivo de icono pueden especificarse como rutas de acceso relativas al directorio donde está instalado el archivo de configuración del formulario.</span><span class="sxs-lookup"><span data-stu-id="eec34-141">Icon file names can be specified as pathnames relative to the directory where the form configuration file is installed.</span></span> <span data-ttu-id="eec34-142">La entrada de la **versión** se usa para indicar el número de versión del formulario.</span><span class="sxs-lookup"><span data-stu-id="eec34-142">The **Version** entry is used to indicate the version number of the form.</span></span> <span data-ttu-id="eec34-143">**Configuración regional** es el identificador de idioma de tres letras de la biblioteca de formulario de destino.</span><span class="sxs-lookup"><span data-stu-id="eec34-143">**Locale** is the three-letter language identifier of the destination form library.</span></span> <span data-ttu-id="eec34-144">Una lista de estos identificadores puede encontrarse en la _referencia del programador de Win32_.</span><span class="sxs-lookup"><span data-stu-id="eec34-144">A list of these identifiers can be found in the  _Win32 Programmer's Reference_.</span></span>
  
<span data-ttu-id="eec34-145">La entrada **oculto** indica si se debe mostrar el formulario en la interfaz de usuario del proveedor de biblioteca de formulario: 1 indica que el archivo está oculto y 0 indica que el formulario está visible.</span><span class="sxs-lookup"><span data-stu-id="eec34-145">The **Hidden** entry indicates whether the form should be displayed in a form library provider's user interface: 1 indicates that the file is hidden and 0 indicates that the form is visible.</span></span> <span data-ttu-id="eec34-146">Se muestra un archivo de configuración del formulario de ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="eec34-146">An example form configuration file is shown following.</span></span> 
  
<span data-ttu-id="eec34-147">La entrada **ComposeInFolder** controla si el formulario está diseñado para colocarse en la carpeta actual o en la Bandeja de entrada del usuario cuando el usuario guarda el mensaje mientras se redacta: 1 indica que el formulario debe ir en la carpeta actual y 0 indica que debe vaya en la Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="eec34-147">The **ComposeInFolder** entry controls whether the form is designed to be placed in the current folder or in the user's Inbox when the user saves the message while composing it: 1 indicates that the form should go in the current folder and 0 indicates that it should go in the Inbox.</span></span> 
  
<span data-ttu-id="eec34-148">La entrada **ComposeCommand** es la cadena que se sitúa en la aplicación cliente del menú de redacción.</span><span class="sxs-lookup"><span data-stu-id="eec34-148">The **ComposeCommand** entry is the string to be placed in the client application's compose menu.</span></span> <span data-ttu-id="eec34-149">Si no se especifica, se usará la entrada **DisplayName** .</span><span class="sxs-lookup"><span data-stu-id="eec34-149">If this is not specified, the **DisplayName** entry will be used.</span></span> 
  
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


