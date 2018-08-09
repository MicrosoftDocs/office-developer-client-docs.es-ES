---
title: Automatizar InfoPath desde una aplicación externa
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d2248d9-ab20-bcaa-d75b-62876c5e95eb
description: Microsoft InfoPath ofrece automatización de aplicación desde el código escrito con COM y secuencias de comandos con los métodos del objeto Application y la colección XDocuments.
ms.openlocfilehash: 0e3fcc50ec11f5fc8791d37144767bf0398ccda7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815757"
---
# <a name="automating-infopath-from-an-external-application"></a><span data-ttu-id="3efda-103">Automatizar InfoPath desde una aplicación externa</span><span class="sxs-lookup"><span data-stu-id="3efda-103">Automating InfoPath from an external application</span></span>

<span data-ttu-id="3efda-104">Microsoft InfoPath ofrece automatización de aplicación desde el código escrito con COM y secuencias de comandos con los métodos del objeto **Application** y la colección **XDocuments** .</span><span class="sxs-lookup"><span data-stu-id="3efda-104">Microsoft InfoPath provides application automation from code written using COM and script by using methods of the **Application** object and the **XDocuments** collection.</span></span> 
  
## <a name="overview-of-the-application-and-xdocument-objects"></a><span data-ttu-id="3efda-105">Información general de la aplicación y los objetos XDocument</span><span class="sxs-lookup"><span data-stu-id="3efda-105">Overview of the Application and XDocument Objects</span></span>

<span data-ttu-id="3efda-106">El objeto **Application** contiene los siguientes métodos empleados para automatización:</span><span class="sxs-lookup"><span data-stu-id="3efda-106">The **Application** object contains the following methods used for automation:</span></span> 
  
|<span data-ttu-id="3efda-107">**Método**</span><span class="sxs-lookup"><span data-stu-id="3efda-107">**Method**</span></span>|<span data-ttu-id="3efda-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3efda-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3efda-109">**CacheSolution**</span><span class="sxs-lookup"><span data-stu-id="3efda-109">**CacheSolution**</span></span> <br/> |<span data-ttu-id="3efda-110">Examina el en la memoria caché y, si es necesario, la actualiza desde la ubicación publicada de la plantilla de formulario.</span><span class="sxs-lookup"><span data-stu-id="3efda-110">Examines the in the cache and, if necessary, updates it from the published location of the form template.</span></span>  <br/> |
|<span data-ttu-id="3efda-111">**Quit**</span><span class="sxs-lookup"><span data-stu-id="3efda-111">**Quit**</span></span> <br/> |<span data-ttu-id="3efda-112">Cierra la aplicación de Microsoft Office InfoPath.</span><span class="sxs-lookup"><span data-stu-id="3efda-112">Quits the Microsoft Office InfoPath application.</span></span>  <br/> |
|<span data-ttu-id="3efda-113">**RegisterSolution**</span><span class="sxs-lookup"><span data-stu-id="3efda-113">**RegisterSolution**</span></span> <br/> |<span data-ttu-id="3efda-114">Instala la plantilla de formulario de Microsoft Office InfoPath especificada.</span><span class="sxs-lookup"><span data-stu-id="3efda-114">Installs the specified Microsoft Office InfoPath form template.</span></span>  <br/> |
|<span data-ttu-id="3efda-115">**UnregisterSolution**</span><span class="sxs-lookup"><span data-stu-id="3efda-115">**UnregisterSolution**</span></span> <br/> |<span data-ttu-id="3efda-116">Desinstala la plantilla de formulario de Microsoft Office InfoPath especificada.</span><span class="sxs-lookup"><span data-stu-id="3efda-116">Uninstalls the specified Microsoft Office InfoPath form template.</span></span>  <br/> |
   
<span data-ttu-id="3efda-117">La colección **XDocuments** contiene los siguientes métodos que se pueden usar para la automatización externa:</span><span class="sxs-lookup"><span data-stu-id="3efda-117">The **XDocuments** collection contains the following methods that can be used for external automation:</span></span> 
  
|<span data-ttu-id="3efda-118">**Método**</span><span class="sxs-lookup"><span data-stu-id="3efda-118">**Method**</span></span>|<span data-ttu-id="3efda-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3efda-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3efda-120">Método **Close**</span><span class="sxs-lookup"><span data-stu-id="3efda-120">**Close** method</span></span>  <br/> |<span data-ttu-id="3efda-121">Cierra el formulario de Microsoft Office InfoPath especificado.</span><span class="sxs-lookup"><span data-stu-id="3efda-121">Closes the specified Microsoft Office InfoPath form.</span></span>  <br/> |
|<span data-ttu-id="3efda-122">**New** (método)</span><span class="sxs-lookup"><span data-stu-id="3efda-122">**New** method</span></span>  <br/> |<span data-ttu-id="3efda-123">Crea un nuevo formulario de Microsoft Office InfoPath.</span><span class="sxs-lookup"><span data-stu-id="3efda-123">Creates a new Microsoft Office InfoPath form.</span></span>  <br/> |
|<span data-ttu-id="3efda-124">Método **NewFromSolution**</span><span class="sxs-lookup"><span data-stu-id="3efda-124">**NewFromSolution** method</span></span>  <br/> |<span data-ttu-id="3efda-125">Crea un nuevo formulario de Microsoft Office InfoPath basado en la plantilla de formulario especificada.</span><span class="sxs-lookup"><span data-stu-id="3efda-125">Creates a new Microsoft Office InfoPath form based on the specified form template.</span></span>  <br/> |
|<span data-ttu-id="3efda-126">Método **NewFromSolutionWithData**</span><span class="sxs-lookup"><span data-stu-id="3efda-126">**NewFromSolutionWithData** method</span></span>  <br/> |<span data-ttu-id="3efda-127">Crea un nuevo formulario de Microsoft Office InfoPath mediante la plantilla de formulario y los datos XML especificada.</span><span class="sxs-lookup"><span data-stu-id="3efda-127">Creates a new Microsoft Office InfoPath form using the specified XML data and form template.</span></span>  <br/> |
|<span data-ttu-id="3efda-128">**Open** (método)</span><span class="sxs-lookup"><span data-stu-id="3efda-128">**Open** method</span></span>  <br/> |<span data-ttu-id="3efda-129">Abre el formulario de Microsoft Office InfoPath especificado.</span><span class="sxs-lookup"><span data-stu-id="3efda-129">Opens the specified Microsoft Office InfoPath form.</span></span>  <br/> |
   
<span data-ttu-id="3efda-130">Para usar el objeto **Application** desde una aplicación externa, utilice la función **CreateObject** con el ProgID de la aplicación InfoPath ("InfoPath.Application") para crear una variable de objeto que representa la aplicación InfoPath.</span><span class="sxs-lookup"><span data-stu-id="3efda-130">To use the **Application** object from an external application, you use the **CreateObject** function with the ProgID of the InfoPath application ("InfoPath.Application") to create an object variable that represents the InfoPath application.</span></span> <span data-ttu-id="3efda-131">A continuación, puede usar la propiedad **XDocuments** para tener acceso a la colección **XDocuments** y usar sus métodos para abrir o crear un formulario de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="3efda-131">You can then use the **XDocuments** property to access the **XDocuments** collection and use its methods to open or create an InfoPath form.</span></span> <span data-ttu-id="3efda-132">En el ejemplo siguiente se muestra la creación de una referencia al objeto **Application** utilizando la 6.0 de Microsoft Visual Basic o Visual Basic para aplicaciones (VBA), lenguaje de programación:</span><span class="sxs-lookup"><span data-stu-id="3efda-132">The following example demonstrates the creation of a reference to the **Application** object using the Microsoft Visual Basic 6.0 or Visual Basic for Applications (VBA) programming language:</span></span> 
  
```vb
Dim objIP As Object 
 
Set objIP = CreateObject("InfoPath.Application") 
 
' Open an existing form 
objIP.XDocuments.Open ("C:\MyFolder\MyForm.xml") 
 
' Create a new form based on a form template 
objIP.XDocuments.NewFromSolution ("C:\MyFolder\MyForm.xsn") 

```

> [!NOTE]
> <span data-ttu-id="3efda-133">Debido a que la función **CreateObject** crea una variable de objeto mediante el enlace, finalización automática de instrucciones no estará disponible en el Editor de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="3efda-133">Because the **CreateObject** function creates an object variable using late binding, automatic statement completion will not be available in the Visual Basic Editor.</span></span> <span data-ttu-id="3efda-134">Hacer referencia a los vínculos en las tablas anteriores para obtener información acerca de la sintaxis llamada correcta.</span><span class="sxs-lookup"><span data-stu-id="3efda-134">Refer to the links in the preceding tables for information about the correct calling syntax.</span></span> 
  

