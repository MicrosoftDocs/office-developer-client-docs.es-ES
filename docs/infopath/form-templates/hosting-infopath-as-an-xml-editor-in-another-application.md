---
title: Hospedar InfoPath como un editor XML en otra aplicación
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ae24b317-f486-763a-7009-e32c5cb85b59
description: El entorno de edición de formulario de Microsoft InfoPath se puede hospedar en una aplicación de Windows personalizada, que permite a los programadores integrar el entorno en aplicaciones de línea de negocio de edición de formularios de InfoPath.
ms.openlocfilehash: dd87cba7219b5647bd2b20dd67c6eb0f1811cc59
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815857"
---
# <a name="hosting-infopath-as-an-xml-editor-in-another-application"></a><span data-ttu-id="9c5fe-103">Hospedar InfoPath como un editor XML en otra aplicación</span><span class="sxs-lookup"><span data-stu-id="9c5fe-103">Hosting InfoPath as an XML Editor in Another Application</span></span>

<span data-ttu-id="9c5fe-p101">El entorno de edición de formularios de Microsoft InfoPath puede hospedarse en una aplicación para Windows personalizada. Esta característica permite a los programadores integrar el entorno de edición de formularios de InfoPath en las aplicaciones de la línea de negocio. Los programadores que crean aplicaciones tradicionales basadas en COM pueden usar el objeto **InfoPathEditorObject**, disponible si se hace referencia a IPEDITOR.DLL, y los programadores que escriben aplicaciones basadas en Microsoft .NET pueden usar el ensamblado **Microsoft.Office.InfoPath.FormControl**, que proporciona tipos administrados basados en la interfaz COM. El archivo IPEDITOR.DLL y el ensamblado **Microsoft.Office.InfoPath.FormControl** se instalan junto con InfoPath en la carpeta C:\Program Files\Microsoft Office\Office15 o C:\Program Files (x86)\Microsoft Office\Office15 .</span><span class="sxs-lookup"><span data-stu-id="9c5fe-p101">The Microsoft InfoPath form editing environment can be hosted in a custom Windows application. This feature enables developers to integrate the InfoPath form editing environment into line-of-business applications. Developers writing traditional COM-based applications can use the **InfoPathEditorObject** object that is available by referencing the IPEDITOR.DLL, and developers writing Microsoft .NET-based applications can use the **Microsoft.Office.InfoPath.FormControl** assembly, which provides managed types based on the COM interface. The IPEDITOR.DLL and **Microsoft.Office.InfoPath.FormControl** assembly are both installed along with InfoPath in the C:\Program Files\Microsoft Office\Office15 or C:\Program Files (x86)\Microsoft Office\Office15 folder.</span></span> 
  
<span data-ttu-id="9c5fe-108">El artículo de MSDN, que hospeda el entorno de edición de formulario de InfoPath 2007 en una aplicación de formularios de Windows personalizada, se centra en el objeto **FormControl** y cómo incorporarla a personalizado. Aplicaciones basadas en red.</span><span class="sxs-lookup"><span data-stu-id="9c5fe-108">The MSDN article, Hosting the InfoPath 2007 Form Editing Environment in a Custom Windows Form Application, focuses on the **FormControl** object and how to incorporate it into your custom .NET-based applications.</span></span> <span data-ttu-id="9c5fe-109">Asociado a este artículo hay una aplicación personalizada que se puede descargar y que ofrece funciones de .NET para replicar el entorno de edición de formularios mediante el uso de **IOleCommandTargets** de COM.</span><span class="sxs-lookup"><span data-stu-id="9c5fe-109">The download associated with the article contains a custom application that provides .NET functions for replicating the InfoPath form editing environment through the use of COM **IOleCommandTargets**.</span></span>
  

