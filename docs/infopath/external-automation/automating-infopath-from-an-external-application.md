---
title: Automatizar InfoPath desde una aplicación externa
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d2248d9-ab20-bcaa-d75b-62876c5e95eb
description: Microsoft InfoPath proporciona automatización de aplicaciones a partir de código escrito con COM y script mediante métodos del objeto Application y la colección XDocuments.
ms.openlocfilehash: 7eccbca34b93aff7909de92eebc04d012d4dd97c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412670"
---
# <a name="automating-infopath-from-an-external-application"></a><span data-ttu-id="f7da2-103">Automatizar InfoPath desde una aplicación externa</span><span class="sxs-lookup"><span data-stu-id="f7da2-103">Automating InfoPath from an external application</span></span>

<span data-ttu-id="f7da2-104">Microsoft InfoPath proporciona automatización de aplicaciones a partir de código escrito con COM y script mediante métodos del **objeto Application** y la **colección XDocuments.**</span><span class="sxs-lookup"><span data-stu-id="f7da2-104">Microsoft InfoPath provides application automation from code written using COM and script by using methods of the **Application** object and the **XDocuments** collection.</span></span> 
  
## <a name="overview-of-the-application-and-xdocument-objects"></a><span data-ttu-id="f7da2-105">Información general sobre los objetos Application y XDocument</span><span class="sxs-lookup"><span data-stu-id="f7da2-105">Overview of the Application and XDocument Objects</span></span>

<span data-ttu-id="f7da2-106">El **objeto Application** contiene los siguientes métodos usados para la automatización:</span><span class="sxs-lookup"><span data-stu-id="f7da2-106">The **Application** object contains the following methods used for automation:</span></span> 
  
|<span data-ttu-id="f7da2-107">**Método**</span><span class="sxs-lookup"><span data-stu-id="f7da2-107">**Method**</span></span>|<span data-ttu-id="f7da2-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f7da2-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f7da2-109">**CacheSolution**</span><span class="sxs-lookup"><span data-stu-id="f7da2-109">**CacheSolution**</span></span> <br/> |<span data-ttu-id="f7da2-110">Examina la memoria caché y, si es necesario, la actualiza desde la ubicación publicada de la plantilla de formulario.</span><span class="sxs-lookup"><span data-stu-id="f7da2-110">Examines the in the cache and, if necessary, updates it from the published location of the form template.</span></span>  <br/> |
|<span data-ttu-id="f7da2-111">**Quit**</span><span class="sxs-lookup"><span data-stu-id="f7da2-111">**Quit**</span></span> <br/> |<span data-ttu-id="f7da2-112">Sale de la Microsoft Office InfoPath.</span><span class="sxs-lookup"><span data-stu-id="f7da2-112">Quits the Microsoft Office InfoPath application.</span></span>  <br/> |
|<span data-ttu-id="f7da2-113">**RegisterSolution**</span><span class="sxs-lookup"><span data-stu-id="f7da2-113">**RegisterSolution**</span></span> <br/> |<span data-ttu-id="f7da2-114">Instala la plantilla de formulario Microsoft Office infoPath especificada.</span><span class="sxs-lookup"><span data-stu-id="f7da2-114">Installs the specified Microsoft Office InfoPath form template.</span></span>  <br/> |
|<span data-ttu-id="f7da2-115">**UnregisterSolution**</span><span class="sxs-lookup"><span data-stu-id="f7da2-115">**UnregisterSolution**</span></span> <br/> |<span data-ttu-id="f7da2-116">Desinstala la plantilla de formulario Microsoft Office infoPath especificada.</span><span class="sxs-lookup"><span data-stu-id="f7da2-116">Uninstalls the specified Microsoft Office InfoPath form template.</span></span>  <br/> |
   
<span data-ttu-id="f7da2-117">La **colección XDocuments** contiene los siguientes métodos que se pueden usar para la automatización externa:</span><span class="sxs-lookup"><span data-stu-id="f7da2-117">The **XDocuments** collection contains the following methods that can be used for external automation:</span></span> 
  
|<span data-ttu-id="f7da2-118">**Método**</span><span class="sxs-lookup"><span data-stu-id="f7da2-118">**Method**</span></span>|<span data-ttu-id="f7da2-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f7da2-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f7da2-120">Método **Close**</span><span class="sxs-lookup"><span data-stu-id="f7da2-120">**Close** method</span></span>  <br/> |<span data-ttu-id="f7da2-121">Cierra el formulario de InfoPath Microsoft Office especificado.</span><span class="sxs-lookup"><span data-stu-id="f7da2-121">Closes the specified Microsoft Office InfoPath form.</span></span>  <br/> |
|<span data-ttu-id="f7da2-122">**Nuevo** método</span><span class="sxs-lookup"><span data-stu-id="f7da2-122">**New** method</span></span>  <br/> |<span data-ttu-id="f7da2-123">Crea un nuevo Microsoft Office de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="f7da2-123">Creates a new Microsoft Office InfoPath form.</span></span>  <br/> |
|<span data-ttu-id="f7da2-124">**NewFromSolution (método)**</span><span class="sxs-lookup"><span data-stu-id="f7da2-124">**NewFromSolution** method</span></span>  <br/> |<span data-ttu-id="f7da2-125">Crea un nuevo Microsoft Office formulario de InfoPath basado en la plantilla de formulario especificada.</span><span class="sxs-lookup"><span data-stu-id="f7da2-125">Creates a new Microsoft Office InfoPath form based on the specified form template.</span></span>  <br/> |
|<span data-ttu-id="f7da2-126">**Método NewFromSolutionWithData**</span><span class="sxs-lookup"><span data-stu-id="f7da2-126">**NewFromSolutionWithData** method</span></span>  <br/> |<span data-ttu-id="f7da2-127">Crea un nuevo Microsoft Office formulario de InfoPath con la plantilla de formulario y los datos XML especificados.</span><span class="sxs-lookup"><span data-stu-id="f7da2-127">Creates a new Microsoft Office InfoPath form using the specified XML data and form template.</span></span>  <br/> |
|<span data-ttu-id="f7da2-128">**Open (método)**</span><span class="sxs-lookup"><span data-stu-id="f7da2-128">**Open** method</span></span>  <br/> |<span data-ttu-id="f7da2-129">Abre el formulario Microsoft Office InfoPath especificado.</span><span class="sxs-lookup"><span data-stu-id="f7da2-129">Opens the specified Microsoft Office InfoPath form.</span></span>  <br/> |
   
<span data-ttu-id="f7da2-130">Para usar el **objeto Application** desde una aplicación externa, use la función **CreateObject** con el ProgID de la aplicación de InfoPath ("InfoPath.Application") para crear una variable de objeto que represente la aplicación de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="f7da2-130">To use the **Application** object from an external application, you use the **CreateObject** function with the ProgID of the InfoPath application ("InfoPath.Application") to create an object variable that represents the InfoPath application.</span></span> <span data-ttu-id="f7da2-131">A continuación, puede usar la **propiedad XDocuments** para obtener acceso a la colección **XDocuments** y usar sus métodos para abrir o crear un formulario de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="f7da2-131">You can then use the **XDocuments** property to access the **XDocuments** collection and use its methods to open or create an InfoPath form.</span></span> <span data-ttu-id="f7da2-132">En el ejemplo siguiente se muestra la creación de una referencia al objeto **Application** mediante el lenguaje de programación microsoft Visual Basic 6.0 o Visual Basic para Aplicaciones (VBA):</span><span class="sxs-lookup"><span data-stu-id="f7da2-132">The following example demonstrates the creation of a reference to the **Application** object using the Microsoft Visual Basic 6.0 or Visual Basic for Applications (VBA) programming language:</span></span> 
  
```vb
Dim objIP As Object 
 
Set objIP = CreateObject("InfoPath.Application") 
 
' Open an existing form 
objIP.XDocuments.Open ("C:\MyFolder\MyForm.xml") 
 
' Create a new form based on a form template 
objIP.XDocuments.NewFromSolution ("C:\MyFolder\MyForm.xsn") 

```

> [!NOTE]
> <span data-ttu-id="f7da2-133">Dado que **la función CreateObject** crea una variable de objeto mediante el enlace en tiempo de ejecución, la finalización automática de instrucciones no estará disponible en el editor Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f7da2-133">Because the **CreateObject** function creates an object variable using late binding, automatic statement completion will not be available in the Visual Basic Editor.</span></span> <span data-ttu-id="f7da2-134">Consulte los vínculos de las tablas anteriores para obtener información sobre la sintaxis de llamada correcta.</span><span class="sxs-lookup"><span data-stu-id="f7da2-134">Refer to the links in the preceding tables for information about the correct calling syntax.</span></span> 
  

