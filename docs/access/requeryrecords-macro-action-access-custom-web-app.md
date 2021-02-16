---
title: Acción de macro RequeryRecords (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1dab102f-24af-4984-8020-a9fb06355639
description: Puede usar la acción RequeryRecords para actualizar, ordenar y filtrar los datos de la vista activa consultando de nuevo el origen de la vista.
ms.openlocfilehash: 69d88401abc0de417f7dc58e275c66f2037212aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439250"
---
# <a name="requeryrecords-macro-action-access-custom-web-app"></a><span data-ttu-id="ac04a-103">Acción de macro RequeryRecords (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="ac04a-103">RequeryRecords Macro Action (Access custom web app)</span></span>

<span data-ttu-id="ac04a-104">Puede usar la acción **RequeryRecords** para actualizar, ordenar y filtrar los datos de la vista activa consultando de nuevo el origen de la vista.</span><span class="sxs-lookup"><span data-stu-id="ac04a-104">You can use the **RequeryRecords** action to refresh, sort, and filter the data in the active view by requerying the source of the view.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="ac04a-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="ac04a-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="ac04a-107">Configuración</span><span class="sxs-lookup"><span data-stu-id="ac04a-107">Setting</span></span>

<span data-ttu-id="ac04a-108">La **acción RequeryRecords** tiene los argumentos siguientes.</span><span class="sxs-lookup"><span data-stu-id="ac04a-108">The **RequeryRecords** action has the following arguments.</span></span> 
  
|<span data-ttu-id="ac04a-109">**Parámetro**</span><span class="sxs-lookup"><span data-stu-id="ac04a-109">**Parameter**</span></span>|<span data-ttu-id="ac04a-110">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="ac04a-110">**Required**</span></span>|<span data-ttu-id="ac04a-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ac04a-111">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ac04a-112">**Where=**</span><span class="sxs-lookup"><span data-stu-id="ac04a-112">**Where=**</span></span> <br/> |<span data-ttu-id="ac04a-113">No</span><span class="sxs-lookup"><span data-stu-id="ac04a-113">No</span></span>  <br/> |<span data-ttu-id="ac04a-114">Una SQL cláusula WHERE que restringe los registros de la vista.</span><span class="sxs-lookup"><span data-stu-id="ac04a-114">A SQL WHERE clause that restricts the records in the view.</span></span> <span data-ttu-id="ac04a-115">De forma predeterminada, este argumento está en blanco.</span><span class="sxs-lookup"><span data-stu-id="ac04a-115">By default, this argument is blank.</span></span>  <br/> |
|<span data-ttu-id="ac04a-116">**OrderBy**</span><span class="sxs-lookup"><span data-stu-id="ac04a-116">**OrderBy**</span></span> <br/> |<span data-ttu-id="ac04a-117">No</span><span class="sxs-lookup"><span data-stu-id="ac04a-117">No</span></span>  <br/> |<span data-ttu-id="ac04a-118">Una expresión de cadena que incluye el nombre del campo o campos en los que se van a ordenar los registros y las palabras clave ASC o DESC opcionales.</span><span class="sxs-lookup"><span data-stu-id="ac04a-118">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span> <span data-ttu-id="ac04a-119">De forma predeterminada, este argumento está en blanco.</span><span class="sxs-lookup"><span data-stu-id="ac04a-119">By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac04a-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ac04a-120">Remarks</span></span>

<span data-ttu-id="ac04a-121">Cualquier ordenación o filtrado aplicado por el usuario se borra cuando se llama a la acción **RequeryRecords.**</span><span class="sxs-lookup"><span data-stu-id="ac04a-121">Any sorting or filtering applied by the user is cleared when the **RequeryRecords** action is called.</span></span> 
  
<span data-ttu-id="ac04a-122">El  *argumento OrderBy*  es el nombre del campo o campos en los que desea ordenar los registros.</span><span class="sxs-lookup"><span data-stu-id="ac04a-122">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="ac04a-123">Si usa más de un nombre de campo, separe los nombres con una coma (,).</span><span class="sxs-lookup"><span data-stu-id="ac04a-123">When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="ac04a-124">Cuando se establece el  *argumento OrderBy,*  los registros se ordenan de forma predeterminada en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="ac04a-124">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  
<span data-ttu-id="ac04a-125">Para ordenar los registros en orden descendente, escriba DESC al final de la expresión del argumento *OrderBy.*</span><span class="sxs-lookup"><span data-stu-id="ac04a-125">To sort records in descending order, enter DESC at the end of the  *OrderBy*  argument expression.</span></span> <span data-ttu-id="ac04a-126">Por ejemplo, para ordenar los registros de clientes en orden descendente por nombre de contacto, establezca el argumento  *OrderBy*  en "ContactName DESC".</span><span class="sxs-lookup"><span data-stu-id="ac04a-126">For example, to sort customer records in descending order by contact name, set the  *OrderBy*  argument to "ContactName DESC".</span></span> 
  
<span data-ttu-id="ac04a-127">Para ordenar los nombres por Apellido descendente y Nombre ascendente, establezca el argumento  *OrderBy*  en "LastName DESC, FirstName ASC".</span><span class="sxs-lookup"><span data-stu-id="ac04a-127">To sort names by LastName descending, and FirstName ascending, set the  *OrderBy*  argument to "LastName DESC, FirstName ASC".</span></span> 
  

