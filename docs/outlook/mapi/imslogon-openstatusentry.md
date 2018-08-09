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
ms.openlocfilehash: 55cf41d251db4c84dad9f12d8f83d0b0dda63ff3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817797"
---
# <a name="imslogonopenstatusentry"></a><span data-ttu-id="0fd69-103">IMSLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="0fd69-103">IMSLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="0fd69-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0fd69-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0fd69-105">Abre un objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="0fd69-105">Opens a status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPVOID FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="0fd69-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0fd69-106">Parameters</span></span>

 <span data-ttu-id="0fd69-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="0fd69-107">_lpInterface_</span></span>
  
> <span data-ttu-id="0fd69-108">[entrada] Un puntero para el identificador de interfaz (IID) para el objeto de estado abrir.</span><span class="sxs-lookup"><span data-stu-id="0fd69-108">[in] A pointer to the interface identifier (IID) for the status object to open.</span></span> <span data-ttu-id="0fd69-109">Paso de NULL indica que se devuelve la interfaz estándar para el objeto (en este caso, la interfaz [IMAPIStatus](imapistatusimapiprop.md) ).</span><span class="sxs-lookup"><span data-stu-id="0fd69-109">Passing NULL indicates the standard interface for the object is returned (in this case, the [IMAPIStatus](imapistatusimapiprop.md) interface).</span></span> <span data-ttu-id="0fd69-110">El parámetro _lpInterface_ también se puede establecer en un identificador para una interfaz adecuada para el objeto.</span><span class="sxs-lookup"><span data-stu-id="0fd69-110">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the object.</span></span> 
    
 <span data-ttu-id="0fd69-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0fd69-111">_ulFlags_</span></span>
  
> <span data-ttu-id="0fd69-112">[entrada] Una máscara de bits de indicadores que controla cómo se abre el objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="0fd69-112">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="0fd69-113">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="0fd69-113">The following flag can be set:</span></span>
    
<span data-ttu-id="0fd69-114">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="0fd69-114">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="0fd69-115">Las solicitudes de permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="0fd69-115">Requests read/write permission.</span></span> <span data-ttu-id="0fd69-116">De forma predeterminada, los objetos se crean con permiso de sólo lectura, y las aplicaciones cliente no deben trabajar en la suposición de que se ha concedido permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="0fd69-116">By default, objects are created with read-only permission, and client applications should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="0fd69-117">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="0fd69-117">_lpulObjType_</span></span>
  
> <span data-ttu-id="0fd69-118">[out] Un puntero al tipo del objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="0fd69-118">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="0fd69-119">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="0fd69-119">_lppEntry_</span></span>
  
> <span data-ttu-id="0fd69-120">[out] Un puntero al puntero para el objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="0fd69-120">[out] A pointer to the pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0fd69-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0fd69-121">Return value</span></span>

<span data-ttu-id="0fd69-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="0fd69-122">S_OK</span></span> 
  
> <span data-ttu-id="0fd69-123">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="0fd69-123">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0fd69-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0fd69-124">Remarks</span></span>

<span data-ttu-id="0fd69-125">Los proveedores de almacén de mensajes implementan el método **IMSLogon::OpenStatusEntry** para abrir un objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="0fd69-125">Message store providers implement the **IMSLogon::OpenStatusEntry** method to open a status object.</span></span> <span data-ttu-id="0fd69-126">A continuación, se utiliza este objeto de estado para que los clientes puedan llamar a los métodos [IMAPIStatus](imapistatusimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="0fd69-126">This status object is then used to enable clients to call [IMAPIStatus](imapistatusimapiprop.md) methods.</span></span> <span data-ttu-id="0fd69-127">Por ejemplo, los clientes pueden utilizar el método [SettingsDialog](imapistatus-settingsdialog.md) para volver a configurar la sesión de inicio de sesión del almacén de mensaje o el método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) para validar el estado de la sesión de inicio de sesión del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0fd69-127">For example, clients can use the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method to reconfigure the message store logon session or the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method to validate the state of the message store logon session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0fd69-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="0fd69-128">See also</span></span>



[<span data-ttu-id="0fd69-129">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0fd69-129">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="0fd69-130">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="0fd69-130">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="0fd69-131">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="0fd69-131">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="0fd69-132">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0fd69-132">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

