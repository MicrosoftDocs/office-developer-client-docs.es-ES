---
title: Acción de Macro OpenPopup (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 850de802-e417-4884-8d14-571de52aa391
description: Se abre la vista especificada en una ventana emergente.
ms.openlocfilehash: 01e0086dc0b54837cf5f095ec6ac5701b5b0b219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815460"
---
# <a name="openpopup-macro-action-access-custom-web-app"></a><span data-ttu-id="ce38e-103">Acción de Macro OpenPopup (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="ce38e-103">OpenPopup Macro Action (Access custom web app)</span></span>

<span data-ttu-id="ce38e-104">Se abre la vista especificada en una ventana emergente.</span><span class="sxs-lookup"><span data-stu-id="ce38e-104">Opens the specified view in a popup window.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="ce38e-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="ce38e-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ce38e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce38e-107">Syntax</span></span>

 <span data-ttu-id="ce38e-108">**OpenPopup** (*Vista*, *donde =*, *Order By*)</span><span class="sxs-lookup"><span data-stu-id="ce38e-108">**OpenPopup** (*View*, *Where=*, *Order By*)</span></span> 
  
<span data-ttu-id="ce38e-109">La acción **OpenPopup** contiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="ce38e-109">The **OpenPopup** action contains the following arguments.</span></span> 
  
|<span data-ttu-id="ce38e-110">**Nombre del argumento**</span><span class="sxs-lookup"><span data-stu-id="ce38e-110">**Argument name**</span></span>|<span data-ttu-id="ce38e-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ce38e-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ce38e-112">*View*</span><span class="sxs-lookup"><span data-stu-id="ce38e-112">*View*</span></span>  <br/> |<span data-ttu-id="ce38e-113">El nombre de la vista que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="ce38e-113">The name of the view to open.</span></span>  <br/> |
| <span data-ttu-id="ce38e-114">*Donde =*</span><span class="sxs-lookup"><span data-stu-id="ce38e-114">*Where=*</span></span>  <br/> |<span data-ttu-id="ce38e-115">Una cláusula WHERE de SQL válida (sin la palabra donde) que restringe los registros en la vista.</span><span class="sxs-lookup"><span data-stu-id="ce38e-115">A valid SQL WHERE clause (without the word WHERE) that restricts the records in the view.</span></span>  <br/> |
| <span data-ttu-id="ce38e-116">*Order By*</span><span class="sxs-lookup"><span data-stu-id="ce38e-116">*Order By*</span></span>  <br/> |<span data-ttu-id="ce38e-117">Una expresión de cadena que incluye el nombre del campo o campos en los que se van a ordenar los registros y las palabras clave ASC o DESC opcionales.</span><span class="sxs-lookup"><span data-stu-id="ce38e-117">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span> <span data-ttu-id="ce38e-118">De forma predeterminada, este argumento está en blanco.</span><span class="sxs-lookup"><span data-stu-id="ce38e-118">By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ce38e-119">Notas</span><span class="sxs-lookup"><span data-stu-id="ce38e-119">Remarks</span></span>

<span data-ttu-id="ce38e-120">La macro actual finaliza una vez que se procesa la acción de **OpenPopup** .</span><span class="sxs-lookup"><span data-stu-id="ce38e-120">The current macro ends once the **OpenPopup** action is processed.</span></span> 
  
<span data-ttu-id="ce38e-121">Ordenación o los filtros aplicados por el usuario está desactivada cuando se llama a la acción **OpenPopup** .</span><span class="sxs-lookup"><span data-stu-id="ce38e-121">Any sorting or filtering applied by the user is cleared when the **OpenPopup** action is called.</span></span> 
  
<span data-ttu-id="ce38e-122">El argumento *OrderBy* es el nombre del campo o campos en el que desea ordenar los registros.</span><span class="sxs-lookup"><span data-stu-id="ce38e-122">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="ce38e-123">Cuando utilice más de un nombre de campo, separe los nombres con una coma (,).</span><span class="sxs-lookup"><span data-stu-id="ce38e-123">When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="ce38e-124">Cuando se establece el argumento *OrderBy* , los registros se ordenan en orden ascendente de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ce38e-124">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  

