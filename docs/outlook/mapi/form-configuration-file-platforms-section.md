---
title: Sección del archivo de configuración de formulario [plataformas]
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3b9b3dc0-4f82-468b-8e77-0374c5b196f4
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7439de5b91cefe89eba2f9395595d4a7c8ca3ec5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419131"
---
# <a name="form-configuration-file-platforms-section"></a><span data-ttu-id="3cade-103">Sección del archivo de configuración de formulario [plataformas]</span><span class="sxs-lookup"><span data-stu-id="3cade-103">Form Configuration File [Platforms] Section</span></span>

<span data-ttu-id="3cade-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3cade-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3cade-105">La sección **[Platforms]** muestra el conjunto completo de plataformas compatibles con este formulario.</span><span class="sxs-lookup"><span data-stu-id="3cade-105">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="3cade-106">Cada entrada de la plataforma consta de la plataforma de prefijo **.**</span><span class="sxs-lookup"><span data-stu-id="3cade-106">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="3cade-107">_String_, donde _String_ es un código de cadena arbitrario de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="3cade-107">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="3cade-108">Cada cadena corresponde a la entrada de la **CPU** de una sección **[Platforms]** individual.</span><span class="sxs-lookup"><span data-stu-id="3cade-108">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="3cade-109">Cada entrada de una sección **[Platforms]** define una _cadena de plataforma_ que hace referencia a una siguiente **[plataforma.**</span><span class="sxs-lookup"><span data-stu-id="3cade-109">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="3cade-110">_cadena_ de la plataforma **]** tal como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="3cade-110">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="3cade-111">La sección **[Platforms]** muestra el conjunto completo de plataformas compatibles con este formulario.</span><span class="sxs-lookup"><span data-stu-id="3cade-111">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="3cade-112">Cada entrada de la plataforma consta de la plataforma de prefijo **.**</span><span class="sxs-lookup"><span data-stu-id="3cade-112">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="3cade-113">_String_, donde _String_ es un código de cadena arbitrario de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="3cade-113">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="3cade-114">Cada cadena corresponde a la entrada de la **CPU** de una sección **[Platforms]** individual.</span><span class="sxs-lookup"><span data-stu-id="3cade-114">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="3cade-115">Cada entrada de una sección **[Platforms]** define una _cadena de plataforma_ que hace referencia a una siguiente **[plataforma.**</span><span class="sxs-lookup"><span data-stu-id="3cade-115">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="3cade-116">_cadena_ de la plataforma **]** tal como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="3cade-116">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="3cade-117">**Select**</span><span class="sxs-lookup"><span data-stu-id="3cade-117">**[Platforms]**</span></span>
  
<span data-ttu-id="3cade-118">**Plataforma**.</span><span class="sxs-lookup"><span data-stu-id="3cade-118">**Platform**.</span></span> <span data-ttu-id="3cade-119">__ =  cadena de_plataforma_ de cadena</span><span class="sxs-lookup"><span data-stu-id="3cade-119">_string_ =  _platform string_</span></span>
  
<span data-ttu-id="3cade-120">A continuación se encuentra un ejemplo de una sección **[Platforms]** .</span><span class="sxs-lookup"><span data-stu-id="3cade-120">Following is an example of a **[Platforms]** section.</span></span> 
  
```cpp
[Platforms]
Platform.1 = NTx86
Platform.2 = Win95

```

<span data-ttu-id="3cade-121">Cada **[plataforma.**</span><span class="sxs-lookup"><span data-stu-id="3cade-121">Each **[Platform.**</span></span> <span data-ttu-id="3cade-122">_cadena_ de la plataforma **]** contiene las dos entradas requeridas, **CPU** y **OSVersion**.</span><span class="sxs-lookup"><span data-stu-id="3cade-122">_platform string_ **]** section contains the two required entries, **CPU** and **OSVersion**.</span></span> <span data-ttu-id="3cade-123">La entrada **CPU** especifica el procesador y la entrada **OSVersion** especifica el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3cade-123">The **CPU** entry specifies the processor, and the **OSVersion** entry specifies the operating system.</span></span> <span data-ttu-id="3cade-124">Los valores de **CPU** válidos se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="3cade-124">Valid **CPU** values are described in the following table.</span></span> 
  
|<span data-ttu-id="3cade-125">**Entrada de CPU**</span><span class="sxs-lookup"><span data-stu-id="3cade-125">**CPU Entry**</span></span>|<span data-ttu-id="3cade-126">**Procesador**</span><span class="sxs-lookup"><span data-stu-id="3cade-126">**Processor**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3cade-127">Ix86</span><span class="sxs-lookup"><span data-stu-id="3cade-127">Ix86</span></span>  <br/> |<span data-ttu-id="3cade-128">Procesadores Intel 80x86 y Pentium series, así como procesadores equivalentes de AMD, Cyrix, NextGen y otros fabricantes.</span><span class="sxs-lookup"><span data-stu-id="3cade-128">Intel 80x86 and Pentium series processors, as well as equivalent processors from AMD, Cyrix, NextGen and other manufacturers.</span></span>  <br/> |
|<span data-ttu-id="3cade-129">MIPS</span><span class="sxs-lookup"><span data-stu-id="3cade-129">MIPS</span></span>  <br/> |<span data-ttu-id="3cade-130">Procesadores MIPS de la serie R4000.</span><span class="sxs-lookup"><span data-stu-id="3cade-130">MIPS R4000 series processors.</span></span>  <br/> |
|<span data-ttu-id="3cade-131">AXP</span><span class="sxs-lookup"><span data-stu-id="3cade-131">AXP</span></span>  <br/> |<span data-ttu-id="3cade-132">Procesador Digital Equipment Corporation Alpha AXP.</span><span class="sxs-lookup"><span data-stu-id="3cade-132">Digital Equipment Corporation Alpha AXP processor.</span></span>  <br/> |
|<span data-ttu-id="3cade-133">PPC</span><span class="sxs-lookup"><span data-stu-id="3cade-133">PPC</span></span>  <br/> |<span data-ttu-id="3cade-134">Procesadores de Motorola Power PC Series.</span><span class="sxs-lookup"><span data-stu-id="3cade-134">Motorola Power PC series processors.</span></span>  <br/> |
|<span data-ttu-id="3cade-135">M68</span><span class="sxs-lookup"><span data-stu-id="3cade-135">M68</span></span>  <br/> |<span data-ttu-id="3cade-136">Mororola procesadores de la serie 68x00.</span><span class="sxs-lookup"><span data-stu-id="3cade-136">Mororola 68x00 series processors.</span></span>  <br/> |
   
<span data-ttu-id="3cade-137">Los valores de **OSVersion** válidos se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="3cade-137">Valid **OSVersion** values are described in the following table.</span></span> 
  
|<span data-ttu-id="3cade-138">**Entrada OSVersion**</span><span class="sxs-lookup"><span data-stu-id="3cade-138">**OSVersion Entry**</span></span>|<span data-ttu-id="3cade-139">**Sistema operativo**</span><span class="sxs-lookup"><span data-stu-id="3cade-139">**Operating System**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3cade-140">Win 3.1</span><span class="sxs-lookup"><span data-stu-id="3cade-140">Win3.1</span></span>  <br/> |<span data-ttu-id="3cade-141">Windows 3,1 y Windows para trabajo en grupo 3,11.</span><span class="sxs-lookup"><span data-stu-id="3cade-141">Windows 3.1 and Windows for Workgroups 3.11.</span></span>  <br/> |
|<span data-ttu-id="3cade-142">Winnt 3.5</span><span class="sxs-lookup"><span data-stu-id="3cade-142">WinNT3.5</span></span>  <br/> |<span data-ttu-id="3cade-143">Windows NT 3,5 o anterior.</span><span class="sxs-lookup"><span data-stu-id="3cade-143">Windows NT 3.5 or lower.</span></span>  <br/> |
|<span data-ttu-id="3cade-144">95</span><span class="sxs-lookup"><span data-stu-id="3cade-144">Win95</span></span>  <br/> |<span data-ttu-id="3cade-145">Windows 95.</span><span class="sxs-lookup"><span data-stu-id="3cade-145">Windows 95.</span></span>  <br/> |
|<span data-ttu-id="3cade-146">WinNT 4.0</span><span class="sxs-lookup"><span data-stu-id="3cade-146">WinNT4.0</span></span>  <br/> |<span data-ttu-id="3cade-147">Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="3cade-147">Windows NT 4.0.</span></span>  <br/> |
|<span data-ttu-id="3cade-148">Mac7</span><span class="sxs-lookup"><span data-stu-id="3cade-148">Mac7</span></span>  <br/> |<span data-ttu-id="3cade-149">Sistema Macintosh 7.</span><span class="sxs-lookup"><span data-stu-id="3cade-149">Macintosh System 7.</span></span>  <br/> |
   
<span data-ttu-id="3cade-150">Además, **[plataforma.**</span><span class="sxs-lookup"><span data-stu-id="3cade-150">Additionally, the **[Platform.**</span></span> <span data-ttu-id="3cade-151">_cadena_ de la plataforma **]** debe contener una entrada **File** o **LinkTo** .</span><span class="sxs-lookup"><span data-stu-id="3cade-151">_platform string_ **]** section must contain either a **File** or **LinkTo** entry.</span></span> <span data-ttu-id="3cade-152">La entrada **File** muestra el archivo ejecutable de la aplicación de servidor de formulario que mantiene la biblioteca de formularios y se carga en un nuevo subdirectorio de la caché de disco cuando se inicia el formulario.</span><span class="sxs-lookup"><span data-stu-id="3cade-152">The **File** entry lists the form server application executable file that the form library maintains and loads into a new subdirectory in the disk cache when the form is launched.</span></span> <span data-ttu-id="3cade-153">Si se \*\*\*\* usa una entrada LinkTo, ésta contiene el nombre de una cadena de plataforma diferente desde la que se toma la información del **archivo** .</span><span class="sxs-lookup"><span data-stu-id="3cade-153">If a **LinkTo** entry is used instead, it contains the name of a different platform string from which the **File** information is taken.</span></span> <span data-ttu-id="3cade-154">Esto es útil si una versión de un formulario admite varias plataformas.</span><span class="sxs-lookup"><span data-stu-id="3cade-154">This is useful if one version of a form supports multiple platforms.</span></span> 
  
<span data-ttu-id="3cade-155">La entrada **del registro** se usa siempre que se utiliza la entrada del **archivo** , identifica la clave del registro de la biblioteca de formularios en la que se almacena el archivo ejecutable de la aplicación de servidor de formularios.</span><span class="sxs-lookup"><span data-stu-id="3cade-155">The **Registry** entry is used whenever the **File** entry is used, it identifies the registry key for the form library where the executable file for the form server application is stored.</span></span> <span data-ttu-id="3cade-156">Las cadenas precedidas por una barra diagonal inversa (\) se colocan en la raíz del registro.</span><span class="sxs-lookup"><span data-stu-id="3cade-156">Strings preceded by a backslash ( \ ) are placed at the root of the registry.</span></span> <span data-ttu-id="3cade-157">Las cadenas que no estén precedidas por una barra diagonal inversa se colocan en la clave del registro HKEY_CLASSES_ROOT\CLSID\ _GUID_\, donde _GUID_ es el **GUID** del formulario.</span><span class="sxs-lookup"><span data-stu-id="3cade-157">Strings not preceded by a backslash are placed in the HKEY_CLASSES_ROOT\CLSID\  _GUID_\ registry key, where  _GUID_ is the **GUID** of the form.</span></span> <span data-ttu-id="3cade-158">Se pueden usar los caracteres "% d" para indicar la ruta de la ruta de directorio desde la que se leyó el archivo de configuración del formulario.</span><span class="sxs-lookup"><span data-stu-id="3cade-158">The characters "%d" can be used to indicate the pathname of the directory from which the form configuration file has been read.</span></span> <span data-ttu-id="3cade-159">Esto es útil para especificar otros archivos con rutas de nombres en relación con el archivo de configuración de formulario.</span><span class="sxs-lookup"><span data-stu-id="3cade-159">This is useful for specifying other files with pathnames relative to the form configuration file.</span></span> <span data-ttu-id="3cade-160">Se pueden especificar varias entradas de **archivo** o **registro** mediante archivo o registro como prefijo seguido de cualquier otro texto.</span><span class="sxs-lookup"><span data-stu-id="3cade-160">**Multiple File** or **Registry** entries can be specified by using File or Registry as a prefix followed by any other text.</span></span> <span data-ttu-id="3cade-161">El formato de **[plataforma.**</span><span class="sxs-lookup"><span data-stu-id="3cade-161">The format for the **[Platform.**</span></span> <span data-ttu-id="3cade-162">_cadena_ de la plataforma **]** es:</span><span class="sxs-lookup"><span data-stu-id="3cade-162">_platform string_ **]** section is:</span></span> 
  
- <span data-ttu-id="3cade-163">**Varias.**</span><span class="sxs-lookup"><span data-stu-id="3cade-163">**[Platform.**</span></span> <span data-ttu-id="3cade-164">_cadena_ de la plataforma **]**</span><span class="sxs-lookup"><span data-stu-id="3cade-164">_platform string_ **]**</span></span>
    
- <span data-ttu-id="3cade-165">\*\*\*\* =  _Cadena_ de CPU</span><span class="sxs-lookup"><span data-stu-id="3cade-165">**CPU** =  _string_</span></span>
    
- <span data-ttu-id="3cade-166">\*\*\*\* =  _Cadena_ OSVersion</span><span class="sxs-lookup"><span data-stu-id="3cade-166">**OSVersion** =  _string_</span></span>
    
- <span data-ttu-id="3cade-167">\*\*\*\* =  _Ruta de acceso_ del archivo</span><span class="sxs-lookup"><span data-stu-id="3cade-167">**File** =  _path_</span></span>
    
- <span data-ttu-id="3cade-168">\*\*\*\* =  _Cadena_ LinkTo</span><span class="sxs-lookup"><span data-stu-id="3cade-168">**LinkTo** =  _string_</span></span>
    
- <span data-ttu-id="3cade-169">**Cadena del registro** =  __</span><span class="sxs-lookup"><span data-stu-id="3cade-169">**Registry** =  _string_</span></span>
  
<span data-ttu-id="3cade-170">A continuación se muestran dos ejemplos **[Platform.**</span><span class="sxs-lookup"><span data-stu-id="3cade-170">The following are two example **[Platform.**</span></span> <span data-ttu-id="3cade-171">_cadena_ de la plataforma **]** secciones, una con la entrada de **archivo** y otra con \*\*\*\* la entrada LinkTo.</span><span class="sxs-lookup"><span data-stu-id="3cade-171">_platform string_ **]** sections, one using the **File** entry and one using the **LinkTo** entry.</span></span> 
  
```cpp
[Platform.NTx86]
CPU = ix86
OSVersion = WinNT3.5
File = \helpdesk.exe
Registry = Local Server = %d\helpdesk.exe
[Platform.Win95]
CPU = ix86
OSVersion = Win95
LinkTo = NTx86

```

<span data-ttu-id="3cade-172">**[Plataforma.**</span><span class="sxs-lookup"><span data-stu-id="3cade-172">The **[Platform.**</span></span> <span data-ttu-id="3cade-173">_cadena_ de la plataforma **]** se omite cuando se agrega un formulario a la biblioteca de formularios local cuando se da por sentado que el instalador ha colocado los archivos que conforman el controlador de clase de mensaje en el almacenamiento local disponible como se indica en la sección del controlador del registro OLE y ha realizado el registro OLE en el registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="3cade-173">_platform string_ **]** section is ignored when adding a form to the local form library, when it is assumed that the installer has placed the files constituting the message class handler into available local storage as named in the handler's section in the OLE registry, and has done the OLE registration in the system's registry.</span></span> 
  

