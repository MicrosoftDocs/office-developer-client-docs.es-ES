---
title: Acción de macro ChangeView (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7eb20f21-0218-4a2c-9bbc-90218a1e87bc
description: Puede usar la acción ChangeView para desplazarse entre las vistas en su ubicación.
ms.openlocfilehash: 0c1e27c264a826d38ec2efbd5be9bc6237ad7437
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282316"
---
# <a name="changeview-macro-action-access-custom-web-app"></a><span data-ttu-id="e6bb4-103">Acción de macro ChangeView (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="e6bb4-103">ChangeView Macro Action (Access custom web app)</span></span>

<span data-ttu-id="e6bb4-104">Puede usar la acción **ChangeView** para desplazarse entre las vistas en su ubicación.</span><span class="sxs-lookup"><span data-stu-id="e6bb4-104">You can use the **ChangeView** action to navigate between views in place.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="e6bb4-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="e6bb4-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="e6bb4-107">Configuración</span><span class="sxs-lookup"><span data-stu-id="e6bb4-107">Setting</span></span>

<span data-ttu-id="e6bb4-108">La acción **ChangeView** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="e6bb4-108">The **ChangeView** action has the following arguments.</span></span> 
  
|<span data-ttu-id="e6bb4-109">**Argumento de la acción**</span><span class="sxs-lookup"><span data-stu-id="e6bb4-109">**Action argument**</span></span>|<span data-ttu-id="e6bb4-110">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="e6bb4-110">**Required**</span></span>|<span data-ttu-id="e6bb4-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e6bb4-111">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e6bb4-112">Table</span><span class="sxs-lookup"><span data-stu-id="e6bb4-112">Table</span></span>  <br/> |<span data-ttu-id="e6bb4-113">Sí</span><span class="sxs-lookup"><span data-stu-id="e6bb4-113">Yes</span></span>  <br/> |<span data-ttu-id="e6bb4-114">Nombre de la tabla que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="e6bb4-114">The name of the table to open.</span></span>  <br/> |
|<span data-ttu-id="e6bb4-115">View</span><span class="sxs-lookup"><span data-stu-id="e6bb4-115">View</span></span>  <br/> |<span data-ttu-id="e6bb4-116">Sí</span><span class="sxs-lookup"><span data-stu-id="e6bb4-116">Yes</span></span>  <br/> |<span data-ttu-id="e6bb4-117">Nombre de la vista que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="e6bb4-117">The name of the view to open.</span></span>  <br/> |
|<span data-ttu-id="e6bb4-118">Donde</span><span class="sxs-lookup"><span data-stu-id="e6bb4-118">Where</span></span>  <br/> |<span data-ttu-id="e6bb4-119">No</span><span class="sxs-lookup"><span data-stu-id="e6bb4-119">No</span></span>  <br/> |<span data-ttu-id="e6bb4-120">Si se especifica, reemplaza la condición WHERE del origen de registros del objeto.</span><span class="sxs-lookup"><span data-stu-id="e6bb4-120">If specified, replaces the Where condition of the object record source.</span></span>  <br/> |
|<span data-ttu-id="e6bb4-121">Ordenar por</span><span class="sxs-lookup"><span data-stu-id="e6bb4-121">Order By</span></span>  <br/> |<span data-ttu-id="e6bb4-122">No</span><span class="sxs-lookup"><span data-stu-id="e6bb4-122">No</span></span>  <br/> |<span data-ttu-id="e6bb4-123">Una expresión de cadena que incluye el nombre del campo o campos en los que se van a ordenar los registros y las palabras clave ASC o DESC opcionales.</span><span class="sxs-lookup"><span data-stu-id="e6bb4-123">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span> <span data-ttu-id="e6bb4-124">De forma predeterminada, este argumento está en blanco.</span><span class="sxs-lookup"><span data-stu-id="e6bb4-124">By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e6bb4-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e6bb4-125">Remarks</span></span>

<span data-ttu-id="e6bb4-126">Las ordenaciones o filtros aplicados por el usuario se borran cuando se llama a la acción **ChangeView** .</span><span class="sxs-lookup"><span data-stu-id="e6bb4-126">Any sorting or filtering applied by the user is cleared when the **ChangeView** action is called.</span></span> 
  
<span data-ttu-id="e6bb4-127">El argumento *OrderBy* es el nombre del campo o campos en los que desea ordenar los registros.</span><span class="sxs-lookup"><span data-stu-id="e6bb4-127">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="e6bb4-128">Si usa más de un nombre de campo, separe los nombres con una coma (,).</span><span class="sxs-lookup"><span data-stu-id="e6bb4-128">When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="e6bb4-129">Cuando se establece el argumento *OrderBy* , los registros se ordenan de forma predeterminada en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="e6bb4-129">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  

