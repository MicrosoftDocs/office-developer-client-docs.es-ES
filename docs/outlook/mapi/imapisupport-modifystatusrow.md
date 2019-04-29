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
ms.openlocfilehash: 8c76e6059670e782ea6530ec8e94f77abfe5b9fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417164"
---
# <a name="imapisupportmodifystatusrow"></a><span data-ttu-id="83a95-103">IMAPISupport::ModifyStatusRow</span><span class="sxs-lookup"><span data-stu-id="83a95-103">IMAPISupport::ModifyStatusRow</span></span>

  
  
<span data-ttu-id="83a95-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="83a95-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="83a95-105">Modifica la tabla de estado agregando una nueva fila o modificando una fila existente.</span><span class="sxs-lookup"><span data-stu-id="83a95-105">Modifies the status table by adding a new row or modifying an existing row.</span></span>
  
```cpp
HRESULT ModifyStatusRow(
ULONG cValues,
LPSPropValue lpColumnVals,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="83a95-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="83a95-106">Parameters</span></span>

 <span data-ttu-id="83a95-107">_cValues_</span><span class="sxs-lookup"><span data-stu-id="83a95-107">_cValues_</span></span>
  
> <span data-ttu-id="83a95-108">a El número de propiedades que se incluirán en la fila de tabla de estado nueva o modificada.</span><span class="sxs-lookup"><span data-stu-id="83a95-108">[in] The count of properties to be included in the new or modified status table row.</span></span> 
    
 <span data-ttu-id="83a95-109">_lpColumnVals_</span><span class="sxs-lookup"><span data-stu-id="83a95-109">_lpColumnVals_</span></span>
  
> <span data-ttu-id="83a95-110">a Un puntero a una matriz de valores de propiedad que describe las propiedades que se incluirán como columnas en la fila de tabla de estado nueva o modificada.</span><span class="sxs-lookup"><span data-stu-id="83a95-110">[in] A pointer to an array of property values that describe the properties to be included as columns in the new or modified status table row.</span></span>
    
 <span data-ttu-id="83a95-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="83a95-111">_ulFlags_</span></span>
  
> <span data-ttu-id="83a95-112">a Máscara de máscara de marcadores que controla cómo se procesa la información que define la fila de la tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="83a95-112">[in] A bitmask of flags that controls how information that defines the status table row is processed.</span></span> <span data-ttu-id="83a95-113">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="83a95-113">The following flag can be set:</span></span>
    
<span data-ttu-id="83a95-114">STATUSROW_UPDATE</span><span class="sxs-lookup"><span data-stu-id="83a95-114">STATUSROW_UPDATE</span></span> 
  
> <span data-ttu-id="83a95-115">Indica a MAPI que combine las propiedades incluidas en la matriz a la que señala _lpColumnVals_ con una fila de tabla de estado existente, en lugar de en una fila nueva.</span><span class="sxs-lookup"><span data-stu-id="83a95-115">Directs MAPI to merge the properties included in the array pointed to by  _lpColumnVals_ with an existing status table row, rather than in a new row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="83a95-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="83a95-116">Return value</span></span>

<span data-ttu-id="83a95-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="83a95-117">S_OK</span></span> 
  
> <span data-ttu-id="83a95-118">La tabla de estado se actualizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="83a95-118">The status table was successfully updated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="83a95-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="83a95-119">Remarks</span></span>

<span data-ttu-id="83a95-120">El método **IMAPISupport:: ModifyStatusRow** se implementa para todos los objetos de compatibilidad del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="83a95-120">The **IMAPISupport::ModifyStatusRow** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="83a95-121">Los proveedores de servicios llaman a **ModifyStatusRow** a la hora de inicio de sesión para agregar una fila a la tabla de estado y en otros momentos durante la sesión para actualizar la fila.</span><span class="sxs-lookup"><span data-stu-id="83a95-121">Service providers call **ModifyStatusRow** at logon time to add a row to the status table and at other times during the session to update the row.</span></span> <span data-ttu-id="83a95-122">**ModifyStatusRow** proporciona a MAPI la información necesaria para crear la tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="83a95-122">**ModifyStatusRow** provides MAPI with the information necessary to build the status table.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="83a95-123">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="83a95-123">Notes to callers</span></span>

<span data-ttu-id="83a95-124">Establezca la marca STATUSROW_UPDATE cuando llame a **ModifyStatusRow** para realizar cambios en las propiedades de la fila de la tabla de estado existente.</span><span class="sxs-lookup"><span data-stu-id="83a95-124">Set the STATUSROW_UPDATE flag when you call **ModifyStatusRow** to make changes to the properties in your existing status table row.</span></span> <span data-ttu-id="83a95-125">Al hacerlo, se indica a MAPI que solo las columnas que se van a cambiar se pasan en el parámetro _lpColumnVals_ .</span><span class="sxs-lookup"><span data-stu-id="83a95-125">Doing so informs MAPI that only the columns being changed are passed in the  _lpColumnVals_ parameter.</span></span> 
  
<span data-ttu-id="83a95-126">Los clientes pueden usar la información de la tabla de estado para obtener acceso al objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="83a95-126">Clients can use the information in the status table to access your status object.</span></span> 
  
<span data-ttu-id="83a95-127">Para obtener una lista completa de las columnas que debe incluir en la fila de la tabla de estado, consulte [TABLE status](status-tables.md).</span><span class="sxs-lookup"><span data-stu-id="83a95-127">For a complete list of columns that you should include in your status table row, see [Status Tables](status-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="83a95-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="83a95-128">See also</span></span>



[<span data-ttu-id="83a95-129">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="83a95-129">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

