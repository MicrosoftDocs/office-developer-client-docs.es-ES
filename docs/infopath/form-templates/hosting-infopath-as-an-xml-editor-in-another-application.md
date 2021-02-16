---
title: Hospedar InfoPath como un editor XML en otra aplicación
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ae24b317-f486-763a-7009-e32c5cb85b59
description: El entorno de edición de formularios de Microsoft InfoPath se puede hospedar en una aplicación de Windows personalizada, lo que permite a los programadores integrar el entorno de edición de formularios de InfoPath en aplicaciones de línea de negocio.
ms.openlocfilehash: b85e47d506b17982bb883c9d56ea13131807d1cf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422582"
---
# <a name="hosting-infopath-as-an-xml-editor-in-another-application"></a><span data-ttu-id="48319-103">Hospedar InfoPath como un editor XML en otra aplicación</span><span class="sxs-lookup"><span data-stu-id="48319-103">Hosting InfoPath as an XML Editor in Another Application</span></span>

<span data-ttu-id="48319-p101">El entorno de edición de formularios de Microsoft InfoPath puede hospedarse en una aplicación para Windows personalizada. Esta característica permite a los programadores integrar el entorno de edición de formularios de InfoPath en las aplicaciones de la línea de negocio. Los programadores que crean aplicaciones tradicionales basadas en COM pueden usar el objeto **InfoPathEditorObject**, disponible si se hace referencia a IPEDITOR.DLL, y los programadores que escriben aplicaciones basadas en Microsoft .NET pueden usar el ensamblado **Microsoft.Office.InfoPath.FormControl**, que proporciona tipos administrados basados en la interfaz COM. El archivo IPEDITOR.DLL y el ensamblado **Microsoft.Office.InfoPath.FormControl** se instalan junto con InfoPath en la carpeta C:\Program Files\Microsoft Office\Office15 o C:\Program Files (x86)\Microsoft Office\Office15 .</span><span class="sxs-lookup"><span data-stu-id="48319-p101">The Microsoft InfoPath form editing environment can be hosted in a custom Windows application. This feature enables developers to integrate the InfoPath form editing environment into line-of-business applications. Developers writing traditional COM-based applications can use the **InfoPathEditorObject** object that is available by referencing the IPEDITOR.DLL, and developers writing Microsoft .NET-based applications can use the **Microsoft.Office.InfoPath.FormControl** assembly, which provides managed types based on the COM interface. The IPEDITOR.DLL and **Microsoft.Office.InfoPath.FormControl** assembly are both installed along with InfoPath in the C:\Program Files\Microsoft Office\Office15 or C:\Program Files (x86)\Microsoft Office\Office15 folder.</span></span> 
  
<span data-ttu-id="48319-108">El artículo de MSDN, que hospeda el entorno de edición de formularios de InfoPath 2007 en una aplicación de formulario personalizada de Windows, se centra en el objeto **FormControl** y en cómo incorporarlo al objeto personalizado . Aplicaciones basadas en NET.</span><span class="sxs-lookup"><span data-stu-id="48319-108">The MSDN article, Hosting the InfoPath 2007 Form Editing Environment in a Custom Windows Form Application, focuses on the **FormControl** object and how to incorporate it into your custom .NET-based applications.</span></span> <span data-ttu-id="48319-109">Asociado a este artículo hay una aplicación personalizada que se puede descargar y que ofrece funciones de .NET para replicar el entorno de edición de formularios mediante el uso de **IOleCommandTargets** de COM.</span><span class="sxs-lookup"><span data-stu-id="48319-109">The download associated with the article contains a custom application that provides .NET functions for replicating the InfoPath form editing environment through the use of COM **IOleCommandTargets**.</span></span>
  

