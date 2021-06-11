---
title: Acción de macro OpenPopup (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 850de802-e417-4884-8d14-571de52aa391
description: Abre la vista especificada en una ventana emergente.
ms.openlocfilehash: 2a8b67fcbf31c42f13b36f06d14d9d046be68c68
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427391"
---
# <a name="openpopup-macro-action-access-custom-web-app"></a><span data-ttu-id="3b288-103">Acción de macro OpenPopup (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="3b288-103">OpenPopup Macro Action (Access custom web app)</span></span>

<span data-ttu-id="3b288-104">Abre la vista especificada en una ventana emergente.</span><span class="sxs-lookup"><span data-stu-id="3b288-104">Opens the specified view in a popup window.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="3b288-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="3b288-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3b288-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b288-107">Syntax</span></span>

 <span data-ttu-id="3b288-108">**OpenPopup** (*View*, *Where=*, *Order By*)</span><span class="sxs-lookup"><span data-stu-id="3b288-108">**OpenPopup** (*View*, *Where=*, *Order By*)</span></span> 
  
<span data-ttu-id="3b288-109">La **acción OpenPopup** contiene los argumentos siguientes.</span><span class="sxs-lookup"><span data-stu-id="3b288-109">The **OpenPopup** action contains the following arguments.</span></span> 
  
|<span data-ttu-id="3b288-110">**Nombre de argumento**</span><span class="sxs-lookup"><span data-stu-id="3b288-110">**Argument name**</span></span>|<span data-ttu-id="3b288-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3b288-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="3b288-112">*View*</span><span class="sxs-lookup"><span data-stu-id="3b288-112">*View*</span></span>  <br/> |<span data-ttu-id="3b288-113">Nombre de la vista que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="3b288-113">The name of the view to open.</span></span>  <br/> |
| <span data-ttu-id="3b288-114">*Where=*</span><span class="sxs-lookup"><span data-stu-id="3b288-114">*Where=*</span></span>  <br/> |<span data-ttu-id="3b288-115">Una cláusula SQL WHERE válida (sin la palabra WHERE) que restringe los registros de la vista.</span><span class="sxs-lookup"><span data-stu-id="3b288-115">A valid SQL WHERE clause (without the word WHERE) that restricts the records in the view.</span></span>  <br/> |
| <span data-ttu-id="3b288-116">*Ordenar por*</span><span class="sxs-lookup"><span data-stu-id="3b288-116">*Order By*</span></span>  <br/> |<span data-ttu-id="3b288-117">Una expresión de cadena que incluye el nombre del campo o campos en los que se van a ordenar los registros y las palabras clave ASC o DESC opcionales.</span><span class="sxs-lookup"><span data-stu-id="3b288-117">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span> <span data-ttu-id="3b288-118">De forma predeterminada, este argumento está en blanco.</span><span class="sxs-lookup"><span data-stu-id="3b288-118">By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3b288-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3b288-119">Remarks</span></span>

<span data-ttu-id="3b288-120">La macro actual finaliza una vez que se procesa la acción **OpenPopup.**</span><span class="sxs-lookup"><span data-stu-id="3b288-120">The current macro ends once the **OpenPopup** action is processed.</span></span> 
  
<span data-ttu-id="3b288-121">Cualquier ordenación o filtrado aplicado por el usuario se borra cuando se llama a la **acción OpenPopup.**</span><span class="sxs-lookup"><span data-stu-id="3b288-121">Any sorting or filtering applied by the user is cleared when the **OpenPopup** action is called.</span></span> 
  
<span data-ttu-id="3b288-122">El  *argumento OrderBy*  es el nombre del campo o campos en los que desea ordenar los registros.</span><span class="sxs-lookup"><span data-stu-id="3b288-122">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="3b288-123">Si usa más de un nombre de campo, separe los nombres con una coma (,).</span><span class="sxs-lookup"><span data-stu-id="3b288-123">When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="3b288-124">Al establecer el argumento  *OrderBy,*  los registros se ordenan de forma predeterminada en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="3b288-124">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  

