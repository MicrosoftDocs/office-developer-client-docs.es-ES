---
title: Referencia para desarrolladores de OneNote
manager: soliver
ms.date: 05/16/2016
ms.audience: Developer
ms.assetid: 4c4ef9e8-6b30-481b-8023-2e1280bcbcc9
description: Esta referencia contiene información general conceptual y referencias de programación para guiarlo en el desarrollo de soluciones para aplicaciones de cliente de escritorio para OneNote 2013.
localization_priority: Priority
ms.openlocfilehash: d2b401a768e62c4b9712b1590bfaf499c2b022ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317055"
---
# <a name="onenote-developer-reference"></a><span data-ttu-id="47d89-103">Referencia para desarrolladores de OneNote</span><span class="sxs-lookup"><span data-stu-id="47d89-103">OneNote developer reference</span></span>

<span data-ttu-id="47d89-104">Esta referencia contiene información general conceptual y referencias de programación para guiarlo en el desarrollo de soluciones para aplicaciones de cliente de escritorio para OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="47d89-104">This reference contains conceptual overviews and programmatic references to guide you in developing solutions for OneNote 2013 desktop client applications.</span></span> <span data-ttu-id="47d89-105">Incluye todas las adiciones y cambios en la interfaz de programación de aplicaciones (API) de OneNote 2013 y proporciona ejemplos de código de C# que muestran cómo realizar algunas tareas en OneNote.</span><span class="sxs-lookup"><span data-stu-id="47d89-105">It includes all the additions and changes to the OneNote 2013 application programming interface (API), and provides code samples in C# to show how to perform some tasks in OneNote.</span></span> <span data-ttu-id="47d89-106">La API de OneNote 2013 permite a los usuarios acceder y modificar el contenido de OneNote mediante programación.</span><span class="sxs-lookup"><span data-stu-id="47d89-106">The OneNote 2013 API enables users to programmatically access and edit OneNote content.</span></span> <span data-ttu-id="47d89-107">Los usuarios también pueden realizar cambios en la vista de ventanas de OneNote.</span><span class="sxs-lookup"><span data-stu-id="47d89-107">Users can also make changes to the view of OneNote windows.</span></span>
  
<span data-ttu-id="47d89-108">Esta documentación contiene la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="47d89-108">This documentation contains the following information:</span></span>
  
- <span data-ttu-id="47d89-109">[Interfaces de ventana](window-interfaces-onenote.md): describe las interfaces **Ventana** y **Ventanas**, que permiten a los usuarios enumerar mediante el conjunto de ventanas de OneNote y modificar ciertas propiedades de estas.</span><span class="sxs-lookup"><span data-stu-id="47d89-109">[Window interfaces](window-interfaces-onenote.md): Describes the **Window** and **Windows** interfaces, which enable users to enumerate through the set of OneNote windows and modify certain window properties.</span></span> 
    
- <span data-ttu-id="47d89-110">[Interfaces del cuadro de diálogo de relleno rápido](quick-filing-dialog-box-interfaces-onenote.md): describen las interfaces que puede usar para personalizar el cuadro de diálogo **Relleno rápido** de OneNote 2013 mediante programación.</span><span class="sxs-lookup"><span data-stu-id="47d89-110">[Quick Filing dialog box interfaces](quick-filing-dialog-box-interfaces-onenote.md): Describes the interfaces that you can use to programmatically customize the **Quick Filing** dialog box in OneNote 2013.</span></span> 
    
- <span data-ttu-id="47d89-111">[Interfaz de la aplicación](application-interface-onenote.md): describe métodos, propiedades y eventos que le ayudan a recuperar, manipular y actualizar información y contenido de OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="47d89-111">[Application interface](application-interface-onenote.md): Describes methods, properties, and events that help retrieve, manipulate, and update OneNote 2013 information and content.</span></span>
    
- <span data-ttu-id="47d89-112">[Enumeraciones](enumerations-onenote-developer-reference.md): describe las enumeraciones del modelo de objetos de OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="47d89-112">[Enumerations](enumerations-onenote-developer-reference.md): Describes the enumerations in the OneNote 2013 object model.</span></span>
    
- <span data-ttu-id="47d89-113">[Códigos de error](error-codes-onenote.md): muestra los códigos de error en el modelo de objetos de OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="47d89-113">[Error codes](error-codes-onenote.md): Lists the error codes in the OneNote 2013 object model.</span></span>
    
> [!NOTE]
> <span data-ttu-id="47d89-114">Las API descritas en esta documentación solo están destinadas para soluciones de cliente de escritorio de OneNote Win32 en escenarios no conectados.</span><span class="sxs-lookup"><span data-stu-id="47d89-114">The APIs described in this documentation are intended only for OneNote Win32 desktop client solutions in unconnected scenarios.</span></span> <span data-ttu-id="47d89-115">Para escenarios conectados, use las API de servicio de OneNote recomendadas.</span><span class="sxs-lookup"><span data-stu-id="47d89-115">For connected scenarios, use the recommended OneNote service APIs.</span></span> <span data-ttu-id="47d89-116">Para obtener más información, visite [dev.onenote.com](https://go.microsoft.com/fwlink/?LinkID=390615).</span><span class="sxs-lookup"><span data-stu-id="47d89-116">To learn more, visit [dev.onenote.com](https://go.microsoft.com/fwlink/?LinkID=390615).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="47d89-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="47d89-117">See also</span></span>

- [<span data-ttu-id="47d89-118">OneNote para desarrolladores</span><span class="sxs-lookup"><span data-stu-id="47d89-118">OneNote for developers</span></span>](https://go.microsoft.com/fwlink/?LinkID=390615)   
- <span data-ttu-id="47d89-119">[Ejemplos de GitHub](https://github.com/OneNoteDev/) (API de servicio de OneNote)</span><span class="sxs-lookup"><span data-stu-id="47d89-119">[Samples on GitHub](https://github.com/OneNoteDev/) (OneNote service APIs)</span></span>     
- [<span data-ttu-id="47d89-120">Accesibilidad en los productos de Microsoft</span><span class="sxs-lookup"><span data-stu-id="47d89-120">Accessibility in Microsoft Products</span></span>](https://www.microsoft.com/enable/products/default.aspx)    
- [<span data-ttu-id="47d89-121">Convenciones del documento</span><span class="sxs-lookup"><span data-stu-id="47d89-121">Document Conventions</span></span>](https://msdn.microsoft.com/office/aa905365.aspx)    
- [<span data-ttu-id="47d89-122">Información de copyright de la referencia para desarrolladores de OneNote</span><span class="sxs-lookup"><span data-stu-id="47d89-122">OneNote Developer Reference Copyright Information</span></span>](https://msdn.microsoft.com/library/office/jj680116.aspx)
    
    

