---
title: IXPLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 261d5f7c-bb61-4e1d-aa41-cca224c63f8e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d9e09de1064a0ae034bb3618f0e5b3719a82c163
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435904"
---
# <a name="ixplogonopenstatusentry"></a><span data-ttu-id="a827f-103">IXPLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="a827f-103">IXPLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="a827f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a827f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a827f-105">Abre el objeto de estado del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="a827f-105">Opens the transport provider's status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="a827f-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="a827f-106">Parameters</span></span>

 <span data-ttu-id="a827f-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="a827f-107">_lpInterface_</span></span>
  
> <span data-ttu-id="a827f-108">[in] Puntero a un identificador de interfaz (IID) para el objeto de inicio de sesión de transporte.</span><span class="sxs-lookup"><span data-stu-id="a827f-108">[in] A pointer to an interface identifier (IID) for the transport logon object.</span></span> <span data-ttu-id="a827f-109">Si se pasa NULL, se [devuelve la interfaz IMAPIStatus.](imapistatusimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="a827f-109">Passing NULL returns the [IMAPIStatus](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="a827f-110">El  _parámetro lpInterface_ también se puede establecer en un identificador de una interfaz para el objeto.</span><span class="sxs-lookup"><span data-stu-id="a827f-110">The  _lpInterface_ parameter can also be set to an identifier for an interface for the object.</span></span> 
    
 <span data-ttu-id="a827f-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a827f-111">_ulFlags_</span></span>
  
> <span data-ttu-id="a827f-112">[in] Máscara de bits de marcas que controla cómo se abre el objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="a827f-112">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="a827f-113">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="a827f-113">The following flag can be set:</span></span>
    
<span data-ttu-id="a827f-114">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="a827f-114">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="a827f-115">Solicitudes de permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="a827f-115">Requests read/write permission.</span></span> <span data-ttu-id="a827f-116">La interfaz predeterminada es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a827f-116">The default interface is read-only.</span></span> 
    
 <span data-ttu-id="a827f-117">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="a827f-117">_lpulObjType_</span></span>
  
> <span data-ttu-id="a827f-118">[salida] Puntero al tipo del objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="a827f-118">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="a827f-119">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="a827f-119">_lppEntry_</span></span>
  
> <span data-ttu-id="a827f-120">[salida] Puntero al puntero al objeto de estado abierto.</span><span class="sxs-lookup"><span data-stu-id="a827f-120">[out] A pointer to the pointer to the opened status object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a827f-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a827f-121">Return value</span></span>

<span data-ttu-id="a827f-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="a827f-122">S_OK</span></span> 
  
> <span data-ttu-id="a827f-123">La llamada se realiza correctamente y devuelve el valor o los valores esperados.</span><span class="sxs-lookup"><span data-stu-id="a827f-123">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a827f-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a827f-124">Remarks</span></span>

<span data-ttu-id="a827f-125">La cola MAPI llama al método **IXPLogon::OpenStatusEntry** cuando una aplicación cliente llama a un método **OpenEntry** para el identificador de entrada en la fila de tabla de estado del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="a827f-125">The MAPI spooler calls the **IXPLogon::OpenStatusEntry** method when a client application calls an **OpenEntry** method for the entry identifier in the transport provider's status table row.</span></span> <span data-ttu-id="a827f-126">**OpenStatusEntry** abre un objeto con la interfaz **IMAPIStatus** asociada a este inicio de sesión del proveedor de transporte en particular.</span><span class="sxs-lookup"><span data-stu-id="a827f-126">**OpenStatusEntry** opens an object with the **IMAPIStatus** interface associated with this particular transport provider logon.</span></span> <span data-ttu-id="a827f-127">A continuación, este objeto se usa para permitir que las aplicaciones cliente llamen a métodos **IMAPIStatus** (por ejemplo, para volver a configurar la sesión de inicio de sesión mediante el método [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) o para validar el estado de la sesión de inicio de sesión mediante el método [IMAPIStatus::ValidateState).](imapistatus-validatestate.md)</span><span class="sxs-lookup"><span data-stu-id="a827f-127">This object is then used to enable client applications to call **IMAPIStatus** methods (for example, to reconfigure the logon session by using the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method, or to validate the state of the logon session by using the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a827f-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="a827f-128">See also</span></span>



[<span data-ttu-id="a827f-129">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a827f-129">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="a827f-130">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a827f-130">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

