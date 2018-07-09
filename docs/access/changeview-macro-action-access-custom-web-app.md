---
title: Acción de Macro ChangeView (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7eb20f21-0218-4a2c-9bbc-90218a1e87bc
description: Puede usar la acción ChangeView para navegar entre vistas en su lugar.
ms.openlocfilehash: c420846074ef362d3388d40ed8700db0739b7ce0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815339"
---
# <a name="changeview-macro-action-access-custom-web-app"></a><span data-ttu-id="03f90-103">Acción de Macro ChangeView (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="03f90-103">ChangeView Macro Action (Access custom web app)</span></span>

<span data-ttu-id="03f90-104">Puede usar la acción **ChangeView** para navegar entre vistas en su lugar.</span><span class="sxs-lookup"><span data-stu-id="03f90-104">You can use the **ChangeView** action to navigate between views in place.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="03f90-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="03f90-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="03f90-107">Configuración</span><span class="sxs-lookup"><span data-stu-id="03f90-107">Setting</span></span>

<span data-ttu-id="03f90-108">La acción **ChangeView** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="03f90-108">The **ChangeView** action has the following arguments.</span></span> 
  
|<span data-ttu-id="03f90-109">**Argumento de la acción**</span><span class="sxs-lookup"><span data-stu-id="03f90-109">**Action argument**</span></span>|<span data-ttu-id="03f90-110">**Necesario**</span><span class="sxs-lookup"><span data-stu-id="03f90-110">**Required**</span></span>|<span data-ttu-id="03f90-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="03f90-111">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="03f90-112">Tabla</span><span class="sxs-lookup"><span data-stu-id="03f90-112">Table</span></span>  <br/> |<span data-ttu-id="03f90-113">Sí</span><span class="sxs-lookup"><span data-stu-id="03f90-113">Yes</span></span>  <br/> |<span data-ttu-id="03f90-114">El nombre de la tabla que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="03f90-114">The name of the table to open.</span></span>  <br/> |
|<span data-ttu-id="03f90-115">Vista</span><span class="sxs-lookup"><span data-stu-id="03f90-115">View</span></span>  <br/> |<span data-ttu-id="03f90-116">Sí</span><span class="sxs-lookup"><span data-stu-id="03f90-116">Yes</span></span>  <br/> |<span data-ttu-id="03f90-117">El nombre de la vista que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="03f90-117">The name of the view to open.</span></span>  <br/> |
|<span data-ttu-id="03f90-118">Donde</span><span class="sxs-lookup"><span data-stu-id="03f90-118">Where</span></span>  <br/> |<span data-ttu-id="03f90-119">No</span><span class="sxs-lookup"><span data-stu-id="03f90-119">No</span></span>  <br/> |<span data-ttu-id="03f90-120">Si se especifica, reemplaza la condición WHERE del origen de registros del objeto.</span><span class="sxs-lookup"><span data-stu-id="03f90-120">If specified, replaces the Where condition of the object record source.</span></span>  <br/> |
|<span data-ttu-id="03f90-121">Order By</span><span class="sxs-lookup"><span data-stu-id="03f90-121">Order By</span></span>  <br/> |<span data-ttu-id="03f90-122">No</span><span class="sxs-lookup"><span data-stu-id="03f90-122">No</span></span>  <br/> |<span data-ttu-id="03f90-123">Una expresión de cadena que incluye el nombre del campo o campos en los que se van a ordenar los registros y las palabras clave ASC o DESC opcionales.</span><span class="sxs-lookup"><span data-stu-id="03f90-123">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span> <span data-ttu-id="03f90-124">De forma predeterminada, este argumento está en blanco.</span><span class="sxs-lookup"><span data-stu-id="03f90-124">By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="03f90-125">Notas</span><span class="sxs-lookup"><span data-stu-id="03f90-125">Remarks</span></span>

<span data-ttu-id="03f90-126">Ordenación o los filtros aplicados por el usuario está desactivada cuando se llama a la acción **ChangeView** .</span><span class="sxs-lookup"><span data-stu-id="03f90-126">Any sorting or filtering applied by the user is cleared when the **ChangeView** action is called.</span></span> 
  
<span data-ttu-id="03f90-127">El argumento *OrderBy* es el nombre del campo o campos en el que desea ordenar los registros.</span><span class="sxs-lookup"><span data-stu-id="03f90-127">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="03f90-128">Cuando utilice más de un nombre de campo, separe los nombres con una coma (,).</span><span class="sxs-lookup"><span data-stu-id="03f90-128">When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="03f90-129">Cuando se establece el argumento *OrderBy* , los registros se ordenan en orden ascendente de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="03f90-129">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  

