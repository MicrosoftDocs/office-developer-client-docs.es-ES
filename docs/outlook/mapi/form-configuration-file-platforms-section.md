---
title: Sección Archivo de configuración de formulario [Plataformas]
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
# <a name="form-configuration-file-platforms-section"></a><span data-ttu-id="3330a-103">Sección Archivo de configuración de formulario [Plataformas]</span><span class="sxs-lookup"><span data-stu-id="3330a-103">Form Configuration File [Platforms] Section</span></span>

<span data-ttu-id="3330a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3330a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3330a-105">La **sección [Plataformas]** enumera el conjunto completo de plataformas admitidas por este formulario.</span><span class="sxs-lookup"><span data-stu-id="3330a-105">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="3330a-106">Cada entrada de plataforma consta del prefijo **Platform.**</span><span class="sxs-lookup"><span data-stu-id="3330a-106">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="3330a-107">_string_, donde  _string_ es un código de cadena arbitrario para la plataforma.</span><span class="sxs-lookup"><span data-stu-id="3330a-107">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="3330a-108">Cada cadena corresponde a la entrada **de CPU** de una sección **individual [Plataformas].**</span><span class="sxs-lookup"><span data-stu-id="3330a-108">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="3330a-109">Cada entrada de una **sección [Plataformas]** define una  _cadena de plataforma_ que hace referencia a una **[Plataforma] posterior.**</span><span class="sxs-lookup"><span data-stu-id="3330a-109">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="3330a-110">_cadena de plataforma_ **]** sección como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="3330a-110">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="3330a-111">La **sección [Plataformas]** enumera el conjunto completo de plataformas admitidas por este formulario.</span><span class="sxs-lookup"><span data-stu-id="3330a-111">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="3330a-112">Cada entrada de plataforma consta del prefijo **Platform.**</span><span class="sxs-lookup"><span data-stu-id="3330a-112">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="3330a-113">_string_, donde  _string_ es un código de cadena arbitrario para la plataforma.</span><span class="sxs-lookup"><span data-stu-id="3330a-113">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="3330a-114">Cada cadena corresponde a la entrada **de CPU** de una sección **individual [Plataformas].**</span><span class="sxs-lookup"><span data-stu-id="3330a-114">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="3330a-115">Cada entrada de una **sección [Plataformas]** define una  _cadena de plataforma_ que hace referencia a una **[Plataforma] posterior.**</span><span class="sxs-lookup"><span data-stu-id="3330a-115">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="3330a-116">_cadena de plataforma_ **]** sección como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="3330a-116">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="3330a-117">**[Plataformas]**</span><span class="sxs-lookup"><span data-stu-id="3330a-117">**[Platforms]**</span></span>
  
<span data-ttu-id="3330a-118">**Plataforma**.</span><span class="sxs-lookup"><span data-stu-id="3330a-118">**Platform**.</span></span> <span data-ttu-id="3330a-119">_string_  =   _cadena de plataforma_</span><span class="sxs-lookup"><span data-stu-id="3330a-119">_string_ =  _platform string_</span></span>
  
<span data-ttu-id="3330a-120">A continuación se muestra un ejemplo de **una sección [Plataformas].**</span><span class="sxs-lookup"><span data-stu-id="3330a-120">Following is an example of a **[Platforms]** section.</span></span> 
  
```cpp
[Platforms]
Platform.1 = NTx86
Platform.2 = Win95

```

<span data-ttu-id="3330a-121">Cada **[Plataforma.**</span><span class="sxs-lookup"><span data-stu-id="3330a-121">Each **[Platform.**</span></span> <span data-ttu-id="3330a-122">_la sección de_ cadena de plataforma **]** contiene las dos entradas necesarias, **CPU** y **OSVersion**.</span><span class="sxs-lookup"><span data-stu-id="3330a-122">_platform string_ **]** section contains the two required entries, **CPU** and **OSVersion**.</span></span> <span data-ttu-id="3330a-123">La **entrada CPU** especifica el procesador y la entrada **OSVersion** especifica el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3330a-123">The **CPU** entry specifies the processor, and the **OSVersion** entry specifies the operating system.</span></span> <span data-ttu-id="3330a-124">Los **valores de CPU** válidos se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="3330a-124">Valid **CPU** values are described in the following table.</span></span> 
  
|<span data-ttu-id="3330a-125">**Entrada de CPU**</span><span class="sxs-lookup"><span data-stu-id="3330a-125">**CPU Entry**</span></span>|<span data-ttu-id="3330a-126">**Procesador**</span><span class="sxs-lookup"><span data-stu-id="3330a-126">**Processor**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3330a-127">Ix86</span><span class="sxs-lookup"><span data-stu-id="3330a-127">Ix86</span></span>  <br/> |<span data-ttu-id="3330a-128">Procesadores de las series Intel 80x86 y Pentium, así como procesadores equivalentes de AMD, Cyrix, NextGen y otros fabricantes.</span><span class="sxs-lookup"><span data-stu-id="3330a-128">Intel 80x86 and Pentium series processors, as well as equivalent processors from AMD, Cyrix, NextGen and other manufacturers.</span></span>  <br/> |
|<span data-ttu-id="3330a-129">MIPS</span><span class="sxs-lookup"><span data-stu-id="3330a-129">MIPS</span></span>  <br/> |<span data-ttu-id="3330a-130">Procesadores de la serie MIPS R4000.</span><span class="sxs-lookup"><span data-stu-id="3330a-130">MIPS R4000 series processors.</span></span>  <br/> |
|<span data-ttu-id="3330a-131">AXP</span><span class="sxs-lookup"><span data-stu-id="3330a-131">AXP</span></span>  <br/> |<span data-ttu-id="3330a-132">Procesador Digital Equipment Corporation Alpha AXP.</span><span class="sxs-lookup"><span data-stu-id="3330a-132">Digital Equipment Corporation Alpha AXP processor.</span></span>  <br/> |
|<span data-ttu-id="3330a-133">PPC</span><span class="sxs-lookup"><span data-stu-id="3330a-133">PPC</span></span>  <br/> |<span data-ttu-id="3330a-134">Procesadores de la serie Power PC de Motorola.</span><span class="sxs-lookup"><span data-stu-id="3330a-134">Motorola Power PC series processors.</span></span>  <br/> |
|<span data-ttu-id="3330a-135">M68</span><span class="sxs-lookup"><span data-stu-id="3330a-135">M68</span></span>  <br/> |<span data-ttu-id="3330a-136">Procesadores de la serie Mororola 68x00.</span><span class="sxs-lookup"><span data-stu-id="3330a-136">Mororola 68x00 series processors.</span></span>  <br/> |
   
<span data-ttu-id="3330a-137">Los **valores válidos de OSVersion** se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="3330a-137">Valid **OSVersion** values are described in the following table.</span></span> 
  
|<span data-ttu-id="3330a-138">**Entrada de OSVersion**</span><span class="sxs-lookup"><span data-stu-id="3330a-138">**OSVersion Entry**</span></span>|<span data-ttu-id="3330a-139">**Sistema operativo**</span><span class="sxs-lookup"><span data-stu-id="3330a-139">**Operating System**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3330a-140">Win3.1</span><span class="sxs-lookup"><span data-stu-id="3330a-140">Win3.1</span></span>  <br/> |<span data-ttu-id="3330a-141">Windows 3.1 y Windows para grupos de trabajo 3.11.</span><span class="sxs-lookup"><span data-stu-id="3330a-141">Windows 3.1 and Windows for Workgroups 3.11.</span></span>  <br/> |
|<span data-ttu-id="3330a-142">WinNT3.5</span><span class="sxs-lookup"><span data-stu-id="3330a-142">WinNT3.5</span></span>  <br/> |<span data-ttu-id="3330a-143">Windows NT 3.5 o inferior.</span><span class="sxs-lookup"><span data-stu-id="3330a-143">Windows NT 3.5 or lower.</span></span>  <br/> |
|<span data-ttu-id="3330a-144">Win95</span><span class="sxs-lookup"><span data-stu-id="3330a-144">Win95</span></span>  <br/> |<span data-ttu-id="3330a-145">Windows 95.</span><span class="sxs-lookup"><span data-stu-id="3330a-145">Windows 95.</span></span>  <br/> |
|<span data-ttu-id="3330a-146">WinNT4.0</span><span class="sxs-lookup"><span data-stu-id="3330a-146">WinNT4.0</span></span>  <br/> |<span data-ttu-id="3330a-147">Windows NT 4.0.</span><span class="sxs-lookup"><span data-stu-id="3330a-147">Windows NT 4.0.</span></span>  <br/> |
|<span data-ttu-id="3330a-148">Mac7</span><span class="sxs-lookup"><span data-stu-id="3330a-148">Mac7</span></span>  <br/> |<span data-ttu-id="3330a-149">Sistema Macintosh 7.</span><span class="sxs-lookup"><span data-stu-id="3330a-149">Macintosh System 7.</span></span>  <br/> |
   
<span data-ttu-id="3330a-150">Además, la **[Plataforma.**</span><span class="sxs-lookup"><span data-stu-id="3330a-150">Additionally, the **[Platform.**</span></span> <span data-ttu-id="3330a-151">_la sección de cadena_ de plataforma **]** debe contener una **entrada File** o **LinkTo.**</span><span class="sxs-lookup"><span data-stu-id="3330a-151">_platform string_ **]** section must contain either a **File** or **LinkTo** entry.</span></span> <span data-ttu-id="3330a-152">La **entrada Archivo** enumera el archivo ejecutable de la aplicación del servidor de formulario que la biblioteca de formularios mantiene y carga en un nuevo subdirectorio de la memoria caché de disco cuando se inicia el formulario.</span><span class="sxs-lookup"><span data-stu-id="3330a-152">The **File** entry lists the form server application executable file that the form library maintains and loads into a new subdirectory in the disk cache when the form is launched.</span></span> <span data-ttu-id="3330a-153">Si se **usa una entrada LinkTo** en su lugar, contiene el nombre de una cadena de plataforma diferente de la que se toma la **información** de archivo.</span><span class="sxs-lookup"><span data-stu-id="3330a-153">If a **LinkTo** entry is used instead, it contains the name of a different platform string from which the **File** information is taken.</span></span> <span data-ttu-id="3330a-154">Esto resulta útil si una versión de un formulario admite varias plataformas.</span><span class="sxs-lookup"><span data-stu-id="3330a-154">This is useful if one version of a form supports multiple platforms.</span></span> 
  
<span data-ttu-id="3330a-155">La **entrada** del Registro  se usa siempre que se usa la entrada Archivo, que identifica la clave del Registro de la biblioteca de formularios donde se almacena el archivo ejecutable de la aplicación del servidor de formularios.</span><span class="sxs-lookup"><span data-stu-id="3330a-155">The **Registry** entry is used whenever the **File** entry is used, it identifies the registry key for the form library where the executable file for the form server application is stored.</span></span> <span data-ttu-id="3330a-156">Las cadenas precedidas por una barra diagonal inversa ( \ ) se colocan en la raíz del Registro.</span><span class="sxs-lookup"><span data-stu-id="3330a-156">Strings preceded by a backslash ( \ ) are placed at the root of the registry.</span></span> <span data-ttu-id="3330a-157">Las cadenas no precedidas por una barra diagonal inversa se colocan en la HKEY_CLASSES_ROOT\CLSID\  _GUID_\ clave del Registro, donde  _GUID_ es el **GUID** del formulario.</span><span class="sxs-lookup"><span data-stu-id="3330a-157">Strings not preceded by a backslash are placed in the HKEY_CLASSES_ROOT\CLSID\  _GUID_\ registry key, where  _GUID_ is the **GUID** of the form.</span></span> <span data-ttu-id="3330a-158">Los caracteres "%d" se pueden usar para indicar el nombre de ruta del directorio desde el que se ha leído el archivo de configuración del formulario.</span><span class="sxs-lookup"><span data-stu-id="3330a-158">The characters "%d" can be used to indicate the pathname of the directory from which the form configuration file has been read.</span></span> <span data-ttu-id="3330a-159">Esto es útil para especificar otros archivos con pathnames relativos al archivo de configuración del formulario.</span><span class="sxs-lookup"><span data-stu-id="3330a-159">This is useful for specifying other files with pathnames relative to the form configuration file.</span></span> <span data-ttu-id="3330a-160">**Se pueden** especificar **varias entradas** de archivo o registro mediante File o Registry como prefijo seguido de cualquier otro texto.</span><span class="sxs-lookup"><span data-stu-id="3330a-160">**Multiple File** or **Registry** entries can be specified by using File or Registry as a prefix followed by any other text.</span></span> <span data-ttu-id="3330a-161">El formato de **la [Plataforma.**</span><span class="sxs-lookup"><span data-stu-id="3330a-161">The format for the **[Platform.**</span></span> <span data-ttu-id="3330a-162">_la sección de cadena de_ plataforma **]** es:</span><span class="sxs-lookup"><span data-stu-id="3330a-162">_platform string_ **]** section is:</span></span> 
  
- <span data-ttu-id="3330a-163">**[Plataforma.**</span><span class="sxs-lookup"><span data-stu-id="3330a-163">**[Platform.**</span></span> <span data-ttu-id="3330a-164">_cadena de plataforma_ **]**</span><span class="sxs-lookup"><span data-stu-id="3330a-164">_platform string_ **]**</span></span>
    
- <span data-ttu-id="3330a-165">**CPU**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="3330a-165">**CPU** =  _string_</span></span>
    
- <span data-ttu-id="3330a-166">**OSVersion**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="3330a-166">**OSVersion** =  _string_</span></span>
    
- <span data-ttu-id="3330a-167">**Archivo**  =   _ruta de acceso_</span><span class="sxs-lookup"><span data-stu-id="3330a-167">**File** =  _path_</span></span>
    
- <span data-ttu-id="3330a-168">**LinkTo**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="3330a-168">**LinkTo** =  _string_</span></span>
    
- <span data-ttu-id="3330a-169">**Registro**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="3330a-169">**Registry** =  _string_</span></span>
  
<span data-ttu-id="3330a-170">A continuación se muestra dos ejemplos **[Platform.**</span><span class="sxs-lookup"><span data-stu-id="3330a-170">The following are two example **[Platform.**</span></span> <span data-ttu-id="3330a-171">_platform string_ **]** sections, one using the **File** entry and one using the **LinkTo** entry.</span><span class="sxs-lookup"><span data-stu-id="3330a-171">_platform string_ **]** sections, one using the **File** entry and one using the **LinkTo** entry.</span></span> 
  
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

<span data-ttu-id="3330a-172">**[Plataforma.**</span><span class="sxs-lookup"><span data-stu-id="3330a-172">The **[Platform.**</span></span> <span data-ttu-id="3330a-173">_la_ sección de cadena de plataforma **]** se omite al agregar un formulario a la biblioteca de formularios local, cuando se supone que el instalador ha colocado los archivos que constituyen el controlador de clase de mensaje en el almacenamiento local disponible como se indica en la sección del controlador en el registro OLE y ha realizado el registro OLE en el registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="3330a-173">_platform string_ **]** section is ignored when adding a form to the local form library, when it is assumed that the installer has placed the files constituting the message class handler into available local storage as named in the handler's section in the OLE registry, and has done the OLE registration in the system's registry.</span></span> 
  

