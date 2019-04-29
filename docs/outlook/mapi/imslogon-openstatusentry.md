---
title: IMSLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 850e256b-6b50-428c-aede-287edaf7b005
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f50c0eb9e3af68e206eaa5bcc51cefa923c30f72
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413181"
---
# <a name="imslogonopenstatusentry"></a><span data-ttu-id="69c53-103">IMSLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="69c53-103">IMSLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="69c53-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69c53-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69c53-105">Abre un objeto status.</span><span class="sxs-lookup"><span data-stu-id="69c53-105">Opens a status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPVOID FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="69c53-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="69c53-106">Parameters</span></span>

 <span data-ttu-id="69c53-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="69c53-107">_lpInterface_</span></span>
  
> <span data-ttu-id="69c53-108">a Un puntero al identificador de interfaz (IID) del objeto status que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="69c53-108">[in] A pointer to the interface identifier (IID) for the status object to open.</span></span> <span data-ttu-id="69c53-109">Si se pasa NULL, se indica la interfaz estándar para el objeto que se devuelve (en este caso, la interfaz [IMAPIStatus](imapistatusimapiprop.md) ).</span><span class="sxs-lookup"><span data-stu-id="69c53-109">Passing NULL indicates the standard interface for the object is returned (in this case, the [IMAPIStatus](imapistatusimapiprop.md) interface).</span></span> <span data-ttu-id="69c53-110">El parámetro _lpInterface_ también se puede establecer en un identificador para una interfaz adecuada para el objeto.</span><span class="sxs-lookup"><span data-stu-id="69c53-110">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the object.</span></span> 
    
 <span data-ttu-id="69c53-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="69c53-111">_ulFlags_</span></span>
  
> <span data-ttu-id="69c53-112">a Máscara de máscara de marcadores que controla cómo se abre el objeto status.</span><span class="sxs-lookup"><span data-stu-id="69c53-112">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="69c53-113">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="69c53-113">The following flag can be set:</span></span>
    
<span data-ttu-id="69c53-114">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="69c53-114">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="69c53-115">Solicita el permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="69c53-115">Requests read/write permission.</span></span> <span data-ttu-id="69c53-116">De forma predeterminada, los objetos se crean con permiso de solo lectura y las aplicaciones cliente no deben funcionar por el supuesto de que se ha concedido el permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="69c53-116">By default, objects are created with read-only permission, and client applications should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="69c53-117">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="69c53-117">_lpulObjType_</span></span>
  
> <span data-ttu-id="69c53-118">contempla Un puntero al tipo del objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="69c53-118">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="69c53-119">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="69c53-119">_lppEntry_</span></span>
  
> <span data-ttu-id="69c53-120">contempla Un puntero al puntero al objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="69c53-120">[out] A pointer to the pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="69c53-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69c53-121">Return value</span></span>

<span data-ttu-id="69c53-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="69c53-122">S_OK</span></span> 
  
> <span data-ttu-id="69c53-123">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="69c53-123">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="69c53-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="69c53-124">Remarks</span></span>

<span data-ttu-id="69c53-125">Los proveedores de almacenamiento de mensajes implementan el método **IMSLogon:: OpenStatusEntry** para abrir un objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="69c53-125">Message store providers implement the **IMSLogon::OpenStatusEntry** method to open a status object.</span></span> <span data-ttu-id="69c53-126">A continuación, este objeto de estado se usa para permitir a los clientes llamar a métodos [IMAPIStatus](imapistatusimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="69c53-126">This status object is then used to enable clients to call [IMAPIStatus](imapistatusimapiprop.md) methods.</span></span> <span data-ttu-id="69c53-127">Por ejemplo, los clientes pueden usar el método [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) para reconfigurar la sesión de inicio del almacén de mensajes o el método [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) para validar el estado de la sesión de inicio del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="69c53-127">For example, clients can use the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method to reconfigure the message store logon session or the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method to validate the state of the message store logon session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="69c53-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="69c53-128">See also</span></span>



[<span data-ttu-id="69c53-129">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="69c53-129">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="69c53-130">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="69c53-130">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="69c53-131">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="69c53-131">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="69c53-132">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="69c53-132">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

