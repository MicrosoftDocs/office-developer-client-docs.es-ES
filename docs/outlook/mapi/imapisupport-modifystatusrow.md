---
title: IMAPISupportModifyStatusRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ModifyStatusRow
api_type:
- COM
ms.assetid: a304ca8f-e404-4535-be76-0b673f2061a0
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 06a5c9de5c0ce4c0f936791086a731a55510a124
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592146"
---
# <a name="imapisupportmodifystatusrow"></a><span data-ttu-id="b524b-103">IMAPISupport::ModifyStatusRow</span><span class="sxs-lookup"><span data-stu-id="b524b-103">IMAPISupport::ModifyStatusRow</span></span>

  
  
<span data-ttu-id="b524b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b524b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b524b-105">Modifica la tabla de estado al agregar una fila nueva o modificar una fila existente.</span><span class="sxs-lookup"><span data-stu-id="b524b-105">Modifies the status table by adding a new row or modifying an existing row.</span></span>
  
```cpp
HRESULT ModifyStatusRow(
ULONG cValues,
LPSPropValue lpColumnVals,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="b524b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b524b-106">Parameters</span></span>

 <span data-ttu-id="b524b-107">_cValues_</span><span class="sxs-lookup"><span data-stu-id="b524b-107">_cValues_</span></span>
  
> <span data-ttu-id="b524b-108">[entrada] El número de propiedades que se deben incluir en la fila de la tabla de estado nuevo o modificado.</span><span class="sxs-lookup"><span data-stu-id="b524b-108">[in] The count of properties to be included in the new or modified status table row.</span></span> 
    
 <span data-ttu-id="b524b-109">_lpColumnVals_</span><span class="sxs-lookup"><span data-stu-id="b524b-109">_lpColumnVals_</span></span>
  
> <span data-ttu-id="b524b-110">[entrada] Un puntero a una matriz de valores de propiedad que se describen las propiedades que se incluirán como columnas en la fila de la tabla de estado nuevo o modificado.</span><span class="sxs-lookup"><span data-stu-id="b524b-110">[in] A pointer to an array of property values that describe the properties to be included as columns in the new or modified status table row.</span></span>
    
 <span data-ttu-id="b524b-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b524b-111">_ulFlags_</span></span>
  
> <span data-ttu-id="b524b-112">[entrada] Una máscara de bits de indicadores que controla cómo se procesa la información que define la fila de la tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="b524b-112">[in] A bitmask of flags that controls how information that defines the status table row is processed.</span></span> <span data-ttu-id="b524b-113">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="b524b-113">The following flag can be set:</span></span>
    
<span data-ttu-id="b524b-114">STATUSROW_UPDATE</span><span class="sxs-lookup"><span data-stu-id="b524b-114">STATUSROW_UPDATE</span></span> 
  
> <span data-ttu-id="b524b-115">Dirige MAPI para combinar las propiedades incluidas en la matriz indicada por _lpColumnVals_ con una fila de tabla de estado existente, en lugar de en una nueva fila.</span><span class="sxs-lookup"><span data-stu-id="b524b-115">Directs MAPI to merge the properties included in the array pointed to by  _lpColumnVals_ with an existing status table row, rather than in a new row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b524b-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b524b-116">Return value</span></span>

<span data-ttu-id="b524b-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="b524b-117">S_OK</span></span> 
  
> <span data-ttu-id="b524b-118">La tabla de estado se ha actualizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="b524b-118">The status table was successfully updated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b524b-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b524b-119">Remarks</span></span>

<span data-ttu-id="b524b-120">El método **IMAPISupport::ModifyStatusRow** se implementa para todos los objetos de soporte técnico de proveedor de servicio.</span><span class="sxs-lookup"><span data-stu-id="b524b-120">The **IMAPISupport::ModifyStatusRow** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="b524b-121">Proveedores de servicios de llamar a **ModifyStatusRow** en tiempo de inicio de sesión para agregar una fila a la tabla de estado y en otros momentos durante la sesión para actualizar la fila.</span><span class="sxs-lookup"><span data-stu-id="b524b-121">Service providers call **ModifyStatusRow** at logon time to add a row to the status table and at other times during the session to update the row.</span></span> <span data-ttu-id="b524b-122">**ModifyStatusRow** proporciona MAPI con la información necesaria para crear la tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="b524b-122">**ModifyStatusRow** provides MAPI with the information necessary to build the status table.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b524b-123">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="b524b-123">Notes to callers</span></span>

<span data-ttu-id="b524b-124">Establecer la marca STATUSROW_UPDATE cuando se llama a **ModifyStatusRow** para realizar cambios en las propiedades de la fila de tabla de estado existente.</span><span class="sxs-lookup"><span data-stu-id="b524b-124">Set the STATUSROW_UPDATE flag when you call **ModifyStatusRow** to make changes to the properties in your existing status table row.</span></span> <span data-ttu-id="b524b-125">Al hacerlo, informa a MAPI que se transfieren sólo las columnas que se va a cambiar en el parámetro _lpColumnVals_ .</span><span class="sxs-lookup"><span data-stu-id="b524b-125">Doing so informs MAPI that only the columns being changed are passed in the  _lpColumnVals_ parameter.</span></span> 
  
<span data-ttu-id="b524b-126">Los clientes pueden usar la información en la tabla de estado para tener acceso a su objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="b524b-126">Clients can use the information in the status table to access your status object.</span></span> 
  
<span data-ttu-id="b524b-127">Para obtener una lista completa de las columnas que se deben incluir en la fila de la tabla de estado, vea [Las tablas de estado](status-tables.md).</span><span class="sxs-lookup"><span data-stu-id="b524b-127">For a complete list of columns that you should include in your status table row, see [Status Tables](status-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b524b-128">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="b524b-128">See also</span></span>



[<span data-ttu-id="b524b-129">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b524b-129">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

