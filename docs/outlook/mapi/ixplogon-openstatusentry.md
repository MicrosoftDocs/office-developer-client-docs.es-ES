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
ms.openlocfilehash: 0e96c0b99f0a5f7511ed59b483ab9409eafad882
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818003"
---
# <a name="ixplogonopenstatusentry"></a><span data-ttu-id="0f75c-103">IXPLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="0f75c-103">IXPLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="0f75c-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0f75c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0f75c-105">Se abre el objeto de estado del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="0f75c-105">Opens the transport provider's status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="0f75c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0f75c-106">Parameters</span></span>

 <span data-ttu-id="0f75c-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="0f75c-107">_lpInterface_</span></span>
  
> <span data-ttu-id="0f75c-108">[entrada] Un puntero a un identificador de interfaz (IID) para el objeto de inicio de sesión de transporte.</span><span class="sxs-lookup"><span data-stu-id="0f75c-108">[in] A pointer to an interface identifier (IID) for the transport logon object.</span></span> <span data-ttu-id="0f75c-109">Pasando NULL, devuelve la interfaz [IMAPIStatus](imapistatusimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="0f75c-109">Passing NULL returns the [IMAPIStatus](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="0f75c-110">El parámetro _lpInterface_ también se puede establecer en un identificador para una interfaz para el objeto.</span><span class="sxs-lookup"><span data-stu-id="0f75c-110">The  _lpInterface_ parameter can also be set to an identifier for an interface for the object.</span></span> 
    
 <span data-ttu-id="0f75c-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0f75c-111">_ulFlags_</span></span>
  
> <span data-ttu-id="0f75c-112">[entrada] Una máscara de bits de indicadores que controla cómo se abre el objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="0f75c-112">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="0f75c-113">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="0f75c-113">The following flag can be set:</span></span>
    
<span data-ttu-id="0f75c-114">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="0f75c-114">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="0f75c-115">Las solicitudes de permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="0f75c-115">Requests read/write permission.</span></span> <span data-ttu-id="0f75c-116">La interfaz predeterminada es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="0f75c-116">The default interface is read-only.</span></span> 
    
 <span data-ttu-id="0f75c-117">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="0f75c-117">_lpulObjType_</span></span>
  
> <span data-ttu-id="0f75c-118">[out] Un puntero al tipo del objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="0f75c-118">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="0f75c-119">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="0f75c-119">_lppEntry_</span></span>
  
> <span data-ttu-id="0f75c-120">[out] Un puntero al puntero para el objeto de estado abierto.</span><span class="sxs-lookup"><span data-stu-id="0f75c-120">[out] A pointer to the pointer to the opened status object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0f75c-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0f75c-121">Return value</span></span>

<span data-ttu-id="0f75c-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="0f75c-122">S_OK</span></span> 
  
> <span data-ttu-id="0f75c-123">La llamada se ha realizado correctamente y devuelve el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="0f75c-123">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0f75c-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0f75c-124">Remarks</span></span>

<span data-ttu-id="0f75c-125">La cola MAPI llama al método de **IXPLogon::OpenStatusEntry** cuando una aplicación cliente llama a un método **OpenEntry** para el identificador de entrada de fila de tabla de estado del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="0f75c-125">The MAPI spooler calls the **IXPLogon::OpenStatusEntry** method when a client application calls an **OpenEntry** method for the entry identifier in the transport provider's status table row.</span></span> <span data-ttu-id="0f75c-126">**OpenStatusEntry** abre un objeto con la interfaz de **IMAPIStatus** asociada a este inicio de sesión del proveedor de transporte determinado.</span><span class="sxs-lookup"><span data-stu-id="0f75c-126">**OpenStatusEntry** opens an object with the **IMAPIStatus** interface associated with this particular transport provider logon.</span></span> <span data-ttu-id="0f75c-127">A continuación, se utiliza este objeto para habilitar las aplicaciones de cliente llamar a métodos **IMAPIStatus** (por ejemplo, para volver a configurar el inicio de sesión mediante el método [SettingsDialog](imapistatus-settingsdialog.md) , o para validar el estado de la sesión de inicio de sesión mediante el uso de la [ IMAPIStatus::ValidateState](imapistatus-validatestate.md) (método)).</span><span class="sxs-lookup"><span data-stu-id="0f75c-127">This object is then used to enable client applications to call **IMAPIStatus** methods (for example, to reconfigure the logon session by using the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method, or to validate the state of the logon session by using the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0f75c-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f75c-128">See also</span></span>



[<span data-ttu-id="0f75c-129">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0f75c-129">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="0f75c-130">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0f75c-130">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

