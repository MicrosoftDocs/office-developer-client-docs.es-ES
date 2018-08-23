---
title: Referencia para desarrolladores de OneNote
manager: soliver
ms.date: 05/16/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4c4ef9e8-6b30-481b-8023-2e1280bcbcc9
description: Esta referencia contiene descripciones conceptuales y las referencias de programación que le guiarán en el desarrollo de soluciones para aplicaciones de cliente de escritorio de OneNote 2013.
ms.openlocfilehash: 6a3dde524dfa5357c4523db3b545ac583eaa3274
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566582"
---
# <a name="onenote-developer-reference"></a><span data-ttu-id="4e2e8-103">Referencia para desarrolladores de OneNote</span><span class="sxs-lookup"><span data-stu-id="4e2e8-103">OneNote developer reference</span></span>

<span data-ttu-id="4e2e8-104">Esta referencia contiene descripciones conceptuales y las referencias de programación que le guiarán en el desarrollo de soluciones para aplicaciones de cliente de escritorio de OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="4e2e8-104">This reference contains conceptual overviews and programmatic references to guide you in developing solutions for OneNote 2013 desktop client applications.</span></span> <span data-ttu-id="4e2e8-105">Incluye todas las adiciones y cambios en la interfaz de programación de aplicaciones (API) de OneNote 2013 y proporciona ejemplos de código de C# que muestran cómo realizar algunas tareas en OneNote.</span><span class="sxs-lookup"><span data-stu-id="4e2e8-105">It includes all the additions and changes to the OneNote 2013 application programming interface (API), and provides code samples in C# to show how to perform some tasks in OneNote.</span></span> <span data-ttu-id="4e2e8-106">La API de OneNote 2013 permite a los usuarios obtener acceso mediante programación y editar el contenido de OneNote.</span><span class="sxs-lookup"><span data-stu-id="4e2e8-106">The OneNote 2013 API enables users to programmatically access and edit OneNote content.</span></span> <span data-ttu-id="4e2e8-107">Los usuarios también pueden realizar cambios a la vista de ventanas de OneNote.</span><span class="sxs-lookup"><span data-stu-id="4e2e8-107">Users can also make changes to the view of OneNote windows.</span></span>
  
<span data-ttu-id="4e2e8-108">Esta documentación contiene la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="4e2e8-108">This documentation contains the following information:</span></span>
  
- <span data-ttu-id="4e2e8-109">[Interfaces de ventana](window-interfaces-onenote.md): se describen las interfaces de **ventana** y de **Windows** , que permiten a los usuarios enumerar el conjunto de ventanas de OneNote y modificar determinadas propiedades de la ventana.</span><span class="sxs-lookup"><span data-stu-id="4e2e8-109">[Window interfaces](window-interfaces-onenote.md): Describes the **Window** and **Windows** interfaces, which enable users to enumerate through the set of OneNote windows and modify certain window properties.</span></span> 
    
- <span data-ttu-id="4e2e8-110">[Interfaces de cuadro de diálogo de archivado rápido](quick-filing-dialog-box-interfaces-onenote.md): se describen las interfaces que puede usar para personalizar mediante programación el cuadro de diálogo **Fiscal rápido** en OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="4e2e8-110">[Quick Filing dialog box interfaces](quick-filing-dialog-box-interfaces-onenote.md): Describes the interfaces that you can use to programmatically customize the **Quick Filing** dialog box in OneNote 2013.</span></span> 
    
- <span data-ttu-id="4e2e8-111">[Interfaz de aplicación](application-interface-onenote.md): se describen los métodos, propiedades y eventos que ayudan a recuperar, manipular y actualizar información de OneNote 2013 y contenido.</span><span class="sxs-lookup"><span data-stu-id="4e2e8-111">[Application interface](application-interface-onenote.md): Describes methods, properties, and events that help retrieve, manipulate, and update OneNote 2013 information and content.</span></span>
    
- <span data-ttu-id="4e2e8-112">[Enumeraciones](enumerations-onenote-developer-reference.md): describe las enumeraciones en el modelo de objetos de OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="4e2e8-112">[Enumerations](enumerations-onenote-developer-reference.md): Describes the enumerations in the OneNote 2013 object model.</span></span>
    
- <span data-ttu-id="4e2e8-113">[Códigos de error](error-codes-onenote.md): se enumeran los códigos de error en el modelo de objetos de OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="4e2e8-113">[Error codes](error-codes-onenote.md): Lists the error codes in the OneNote 2013 object model.</span></span>
    
> [!NOTE]
> <span data-ttu-id="4e2e8-114">Las API descritas en esta documentación solo están destinadas para soluciones de cliente de escritorio de OneNote Win32 en escenarios no conectados.</span><span class="sxs-lookup"><span data-stu-id="4e2e8-114">The APIs described in this documentation are intended only for OneNote Win32 desktop client solutions in unconnected scenarios.</span></span> <span data-ttu-id="4e2e8-115">Para escenarios conectados, use las API de servicio de OneNote recomendadas.</span><span class="sxs-lookup"><span data-stu-id="4e2e8-115">For connected scenarios, use the recommended OneNote service APIs.</span></span> <span data-ttu-id="4e2e8-116">Para obtener más información, visite [dev.onenote.com](http://go.microsoft.com/fwlink/?LinkID=390615).</span><span class="sxs-lookup"><span data-stu-id="4e2e8-116">To learn more, visit [dev.onenote.com](http://go.microsoft.com/fwlink/?LinkID=390615).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4e2e8-117">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="4e2e8-117">See also</span></span>

- [<span data-ttu-id="4e2e8-118">OneNote para desarrolladores</span><span class="sxs-lookup"><span data-stu-id="4e2e8-118">OneNote for developers</span></span>](http://go.microsoft.com/fwlink/?LinkID=390615)   
- <span data-ttu-id="4e2e8-119">[Ejemplos en depósito](https://github.com/OneNoteDev/) (API de OneNote service)</span><span class="sxs-lookup"><span data-stu-id="4e2e8-119">[Samples on GitHub](https://github.com/OneNoteDev/) (OneNote service APIs)</span></span>     
- [<span data-ttu-id="4e2e8-120">Accesibilidad en productos de Microsoft</span><span class="sxs-lookup"><span data-stu-id="4e2e8-120">Accessibility in Microsoft Products</span></span>](http://www.microsoft.com/enable/products/default.aspx)    
- [<span data-ttu-id="4e2e8-121">Convenciones de documentos</span><span class="sxs-lookup"><span data-stu-id="4e2e8-121">Document Conventions</span></span>](http://msdn.microsoft.com/en-us/office/aa905365.aspx)    
- [<span data-ttu-id="4e2e8-122">Información de Copyright de referencia para desarrolladores de OneNote</span><span class="sxs-lookup"><span data-stu-id="4e2e8-122">OneNote Developer Reference Copyright Information</span></span>](https://msdn.microsoft.com/en-us/library/office/jj680116.aspx)
    
    

