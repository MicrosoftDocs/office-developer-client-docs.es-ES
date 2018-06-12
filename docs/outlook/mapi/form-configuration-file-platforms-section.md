---
title: Sección de [plataformas] del archivo de configuración de formulario
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3b9b3dc0-4f82-468b-8e77-0374c5b196f4
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: ddc6db2303d9d5f114fdb27b6e15e699a04e73f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816853"
---
# <a name="form-configuration-file-platforms-section"></a><span data-ttu-id="e23cb-103">Sección de [plataformas] del archivo de configuración de formulario</span><span class="sxs-lookup"><span data-stu-id="e23cb-103">Form Configuration File [Platforms] Section</span></span>

<span data-ttu-id="e23cb-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e23cb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e23cb-105">La sección **[plataformas]** enumera el conjunto completo de plataformas compatibles con este formulario.</span><span class="sxs-lookup"><span data-stu-id="e23cb-105">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="e23cb-106">Cada entrada de plataforma consta del prefijo **plataforma.**</span><span class="sxs-lookup"><span data-stu-id="e23cb-106">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="e23cb-107">_cadena_, donde la _cadena_ es un código de cadena arbitraria para la plataforma</span><span class="sxs-lookup"><span data-stu-id="e23cb-107">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="e23cb-108">Cada cadena corresponde a la entrada de **CPU** de un secciones **[plataformas]** individuales.</span><span class="sxs-lookup"><span data-stu-id="e23cb-108">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="e23cb-109">Cada entrada en una sección **[plataformas]** define una _cadena de la plataforma_ que hace referencia a una posterior **[plataforma.**</span><span class="sxs-lookup"><span data-stu-id="e23cb-109">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="e23cb-110">_cadena de plataforma_ sección de **]** tal como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="e23cb-110">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="e23cb-111">La sección **[plataformas]** enumera el conjunto completo de plataformas compatibles con este formulario.</span><span class="sxs-lookup"><span data-stu-id="e23cb-111">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="e23cb-112">Cada entrada de plataforma consta del prefijo **plataforma.**</span><span class="sxs-lookup"><span data-stu-id="e23cb-112">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="e23cb-113">_cadena_, donde la _cadena_ es un código de cadena arbitraria para la plataforma</span><span class="sxs-lookup"><span data-stu-id="e23cb-113">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="e23cb-114">Cada cadena corresponde a la entrada de **CPU** de un secciones **[plataformas]** individuales.</span><span class="sxs-lookup"><span data-stu-id="e23cb-114">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="e23cb-115">Cada entrada en una sección **[plataformas]** define una _cadena de la plataforma_ que hace referencia a una posterior **[plataforma.**</span><span class="sxs-lookup"><span data-stu-id="e23cb-115">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="e23cb-116">_cadena de plataforma_ sección de **]** tal como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="e23cb-116">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="e23cb-117">**[Plataformas]**</span><span class="sxs-lookup"><span data-stu-id="e23cb-117">**[Platforms]**</span></span>
  
<span data-ttu-id="e23cb-118">**Plataforma**.</span><span class="sxs-lookup"><span data-stu-id="e23cb-118">**Platform**.</span></span> <span data-ttu-id="e23cb-119">_cadena_ =  _cadena de plataforma_</span><span class="sxs-lookup"><span data-stu-id="e23cb-119">_string_ =  _platform string_</span></span>
  
<span data-ttu-id="e23cb-120">Siguiente es un ejemplo de una sección **[plataformas]** .</span><span class="sxs-lookup"><span data-stu-id="e23cb-120">Following is an example of a **[Platforms]** section.</span></span> 
  
```cpp
[Platforms]
Platform.1 = NTx86
Platform.2 = Win95

```

<span data-ttu-id="e23cb-121">Cada **[plataforma.**</span><span class="sxs-lookup"><span data-stu-id="e23cb-121">Each **[Platform.**</span></span> <span data-ttu-id="e23cb-122">_cadena de plataforma_ sección **]** contiene las dos entradas necesarias, **CPU** y **OSVersion**.</span><span class="sxs-lookup"><span data-stu-id="e23cb-122">_platform string_ **]** section contains the two required entries, **CPU** and **OSVersion**.</span></span> <span data-ttu-id="e23cb-123">La entrada de **CPU** especifica el procesador, y la entrada **OSVersion** especifica el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e23cb-123">The **CPU** entry specifies the processor, and the **OSVersion** entry specifies the operating system.</span></span> <span data-ttu-id="e23cb-124">Los valores válidos de **CPU** se describen en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="e23cb-124">Valid **CPU** values are described in the following table.</span></span> 
  
|<span data-ttu-id="e23cb-125">**Entrada de CPU**</span><span class="sxs-lookup"><span data-stu-id="e23cb-125">**CPU Entry**</span></span>|<span data-ttu-id="e23cb-126">**Procesador**</span><span class="sxs-lookup"><span data-stu-id="e23cb-126">**Processor**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e23cb-127">Ix86</span><span class="sxs-lookup"><span data-stu-id="e23cb-127">Ix86</span></span>  <br/> |<span data-ttu-id="e23cb-128">Intel 80 x 86 y procesadores Pentium de la serie, así como los procesadores equivalentes de AMD, Cyrix, NextGen y otros fabricantes.</span><span class="sxs-lookup"><span data-stu-id="e23cb-128">Intel 80x86 and Pentium series processors, as well as equivalent processors from AMD, Cyrix, NextGen and other manufacturers.</span></span>  <br/> |
|<span data-ttu-id="e23cb-129">MIPS</span><span class="sxs-lookup"><span data-stu-id="e23cb-129">MIPS</span></span>  <br/> |<span data-ttu-id="e23cb-130">Procesadores de la serie de MIPS R4000.</span><span class="sxs-lookup"><span data-stu-id="e23cb-130">MIPS R4000 series processors.</span></span>  <br/> |
|<span data-ttu-id="e23cb-131">AXP</span><span class="sxs-lookup"><span data-stu-id="e23cb-131">AXP</span></span>  <br/> |<span data-ttu-id="e23cb-132">Procesador Digital Equipment Corporation Alpha AXP.</span><span class="sxs-lookup"><span data-stu-id="e23cb-132">Digital Equipment Corporation Alpha AXP processor.</span></span>  <br/> |
|<span data-ttu-id="e23cb-133">PPC</span><span class="sxs-lookup"><span data-stu-id="e23cb-133">PPC</span></span>  <br/> |<span data-ttu-id="e23cb-134">Procesadores de la serie de Motorola Power PC.</span><span class="sxs-lookup"><span data-stu-id="e23cb-134">Motorola Power PC series processors.</span></span>  <br/> |
|<span data-ttu-id="e23cb-135">M68</span><span class="sxs-lookup"><span data-stu-id="e23cb-135">M68</span></span>  <br/> |<span data-ttu-id="e23cb-136">Procesadores de la serie Mororola 68 x 00.</span><span class="sxs-lookup"><span data-stu-id="e23cb-136">Mororola 68x00 series processors.</span></span>  <br/> |
   
<span data-ttu-id="e23cb-137">Los valores válidos de **OSVersion** se describen en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="e23cb-137">Valid **OSVersion** values are described in the following table.</span></span> 
  
|<span data-ttu-id="e23cb-138">**Entrada de OSVersion**</span><span class="sxs-lookup"><span data-stu-id="e23cb-138">**OSVersion Entry**</span></span>|<span data-ttu-id="e23cb-139">**Sistema operativo**</span><span class="sxs-lookup"><span data-stu-id="e23cb-139">**Operating System**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e23cb-140">Win3.1</span><span class="sxs-lookup"><span data-stu-id="e23cb-140">Win3.1</span></span>  <br/> |<span data-ttu-id="e23cb-141">Windows 3.1 y Windows para trabajo en grupo 3.11.</span><span class="sxs-lookup"><span data-stu-id="e23cb-141">Windows 3.1 and Windows for Workgroups 3.11.</span></span>  <br/> |
|<span data-ttu-id="e23cb-142">WinNT3.5</span><span class="sxs-lookup"><span data-stu-id="e23cb-142">WinNT3.5</span></span>  <br/> |<span data-ttu-id="e23cb-143">Windows NT 3.5 o inferior.</span><span class="sxs-lookup"><span data-stu-id="e23cb-143">Windows NT 3.5 or lower.</span></span>  <br/> |
|<span data-ttu-id="e23cb-144">Windows 95</span><span class="sxs-lookup"><span data-stu-id="e23cb-144">Win95</span></span>  <br/> |<span data-ttu-id="e23cb-145">Windows 95.</span><span class="sxs-lookup"><span data-stu-id="e23cb-145">Windows 95.</span></span>  <br/> |
|<span data-ttu-id="e23cb-146">WinNT4.0</span><span class="sxs-lookup"><span data-stu-id="e23cb-146">WinNT4.0</span></span>  <br/> |<span data-ttu-id="e23cb-147">Windows NT 4.0.</span><span class="sxs-lookup"><span data-stu-id="e23cb-147">Windows NT 4.0.</span></span>  <br/> |
|<span data-ttu-id="e23cb-148">Mac7</span><span class="sxs-lookup"><span data-stu-id="e23cb-148">Mac7</span></span>  <br/> |<span data-ttu-id="e23cb-149">Sistema de Macintosh 7.</span><span class="sxs-lookup"><span data-stu-id="e23cb-149">Macintosh System 7.</span></span>  <br/> |
   
<span data-ttu-id="e23cb-150">Además, el **[plataforma.**</span><span class="sxs-lookup"><span data-stu-id="e23cb-150">Additionally, the **[Platform.**</span></span> <span data-ttu-id="e23cb-151">_cadena de plataforma_ sección **]** debe contener una entrada de un **archivo** o **enlacesa** .</span><span class="sxs-lookup"><span data-stu-id="e23cb-151">_platform string_ **]** section must contain either a **File** or **LinkTo** entry.</span></span> <span data-ttu-id="e23cb-152">La entrada de **archivo** enumera el archivo ejecutable de aplicación de servidor de formulario que mantiene la biblioteca de formularios y se carga en un subdirectorio nuevo en la caché de disco cuando se inicia el formulario.</span><span class="sxs-lookup"><span data-stu-id="e23cb-152">The **File** entry lists the form server application executable file that the form library maintains and loads into a new subdirectory in the disk cache when the form is launched.</span></span> <span data-ttu-id="e23cb-153">Si una entrada **enlacesa** se usa en su lugar, contiene el nombre de una cadena de plataforma diferente de la que se toma la información del **archivo** .</span><span class="sxs-lookup"><span data-stu-id="e23cb-153">If a **LinkTo** entry is used instead, it contains the name of a different platform string from which the **File** information is taken.</span></span> <span data-ttu-id="e23cb-154">Esto es útil si una versión de un formulario es compatible con varias plataformas.</span><span class="sxs-lookup"><span data-stu-id="e23cb-154">This is useful if one version of a form supports multiple platforms.</span></span> 
  
<span data-ttu-id="e23cb-155">La entrada **del registro** se usa siempre que se utiliza la entrada de **archivo** , identifica la clave del registro de la biblioteca de formularios donde se almacena el archivo ejecutable de la aplicación de servidor del formulario.</span><span class="sxs-lookup"><span data-stu-id="e23cb-155">The **Registry** entry is used whenever the **File** entry is used, it identifies the registry key for the form library where the executable file for the form server application is stored.</span></span> <span data-ttu-id="e23cb-156">Cadenas precedidas por una barra diagonal inversa (\) se colocan en la raíz del registro.</span><span class="sxs-lookup"><span data-stu-id="e23cb-156">Strings preceded by a backslash ( \ ) are placed at the root of the registry.</span></span> <span data-ttu-id="e23cb-157">Las cadenas no precedidas por una barra diagonal inversa se colocan en el _GUID_de HKEY_CLASSES_ROOT\CLSID\ \ clave del registro, donde _GUID_ es el **GUID** del formulario.</span><span class="sxs-lookup"><span data-stu-id="e23cb-157">Strings not preceded by a backslash are placed in the HKEY_CLASSES_ROOT\CLSID\  _GUID_\ registry key, where  _GUID_ is the **GUID** of the form.</span></span> <span data-ttu-id="e23cb-158">Los caracteres "%d" pueden utilizarse para indicar la ruta de acceso del directorio desde el que se ha leído el archivo de configuración del formulario.</span><span class="sxs-lookup"><span data-stu-id="e23cb-158">The characters "%d" can be used to indicate the pathname of the directory from which the form configuration file has been read.</span></span> <span data-ttu-id="e23cb-159">Esto es útil para especificar otros archivos con nombres de ruta de acceso relativa al archivo de configuración del formulario.</span><span class="sxs-lookup"><span data-stu-id="e23cb-159">This is useful for specifying other files with pathnames relative to the form configuration file.</span></span> <span data-ttu-id="e23cb-160">Las entradas de **registro** o **Varios archivos** se pueden especificar mediante el uso del registro o archivo como un prefijo seguido de cualquier otro texto.</span><span class="sxs-lookup"><span data-stu-id="e23cb-160">**Multiple File** or **Registry** entries can be specified by using File or Registry as a prefix followed by any other text.</span></span> <span data-ttu-id="e23cb-161">El formato para el **[plataforma.**</span><span class="sxs-lookup"><span data-stu-id="e23cb-161">The format for the **[Platform.**</span></span> <span data-ttu-id="e23cb-162">_cadena de plataforma_ sección **]** es:</span><span class="sxs-lookup"><span data-stu-id="e23cb-162">_platform string_ **]** section is:</span></span> 
  
- <span data-ttu-id="e23cb-163">**[Plataforma.**</span><span class="sxs-lookup"><span data-stu-id="e23cb-163">**[Platform.**</span></span> <span data-ttu-id="e23cb-164">_cadena de plataforma_ **]**</span><span class="sxs-lookup"><span data-stu-id="e23cb-164">_platform string_ **]**</span></span>
    
- <span data-ttu-id="e23cb-165">**CPU** =  _cadena_</span><span class="sxs-lookup"><span data-stu-id="e23cb-165">**CPU** =  _string_</span></span>
    
- <span data-ttu-id="e23cb-166">**OSVersion** =  _cadena_</span><span class="sxs-lookup"><span data-stu-id="e23cb-166">**OSVersion** =  _string_</span></span>
    
- <span data-ttu-id="e23cb-167">**Archivo** =  _ruta de acceso_</span><span class="sxs-lookup"><span data-stu-id="e23cb-167">**File** =  _path_</span></span>
    
- <span data-ttu-id="e23cb-168">**Enlacesa** =  _cadena_</span><span class="sxs-lookup"><span data-stu-id="e23cb-168">**LinkTo** =  _string_</span></span>
    
- <span data-ttu-id="e23cb-169">**El registro** =  _cadena_</span><span class="sxs-lookup"><span data-stu-id="e23cb-169">**Registry** =  _string_</span></span>
  
<span data-ttu-id="e23cb-170">Los siguientes son dos ejemplo **[plataforma.**</span><span class="sxs-lookup"><span data-stu-id="e23cb-170">The following are two example **[Platform.**</span></span> <span data-ttu-id="e23cb-171">_cadena de plataforma_ en las secciones **]** , uno con la entrada del **archivo** y uno con la entrada **enlacesa** .</span><span class="sxs-lookup"><span data-stu-id="e23cb-171">_platform string_ **]** sections, one using the **File** entry and one using the **LinkTo** entry.</span></span> 
  
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

<span data-ttu-id="e23cb-172">El **[plataforma.**</span><span class="sxs-lookup"><span data-stu-id="e23cb-172">The **[Platform.**</span></span> <span data-ttu-id="e23cb-173">_cadena de plataforma_ sección **]** se omite cuando se agrega un formulario a la biblioteca de formularios local, cuando se supone que el programa de instalación colocó los archivos que constituyen el controlador de clase de mensaje a un almacenamiento local disponible como con nombre en la sección del controlador en el registro OLE y ha realizado el registro OLE en el registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="e23cb-173">_platform string_ **]** section is ignored when adding a form to the local form library, when it is assumed that the installer has placed the files constituting the message class handler into available local storage as named in the handler's section in the OLE registry, and has done the OLE registration in the system's registry.</span></span> 
  

