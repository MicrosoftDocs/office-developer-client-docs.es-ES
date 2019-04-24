---
title: IXPLogonValidateState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.ValidateState
api_type:
- COM
ms.assetid: c3649daa-cba1-48e3-9ffb-069c1bcf8228
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a3469e6baacb52938b870ca87d824bf640a8a88f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351572"
---
# <a name="ixplogonvalidatestate"></a><span data-ttu-id="22e12-103">IXPLogon::ValidateState</span><span class="sxs-lookup"><span data-stu-id="22e12-103">IXPLogon::ValidateState</span></span>

  
  
<span data-ttu-id="22e12-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22e12-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22e12-105">Comprueba el estado externo del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="22e12-105">Checks the transport provider's external status.</span></span> 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="22e12-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="22e12-106">Parameters</span></span>

 <span data-ttu-id="22e12-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="22e12-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="22e12-108">a Identificador de la ventana primaria de los cuadros de diálogo o ventanas que muestra este método.</span><span class="sxs-lookup"><span data-stu-id="22e12-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="22e12-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="22e12-109">_ulFlags_</span></span>
  
> <span data-ttu-id="22e12-110">a Una máscara de máscara de marcadores que controla cómo se realiza la comprobación de estado y los resultados de la comprobación de estado.</span><span class="sxs-lookup"><span data-stu-id="22e12-110">[in] A bitmask of flags that controls how the status check is performed and the results of the status check.</span></span> <span data-ttu-id="22e12-111">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="22e12-111">The following flags can be set:</span></span>
    
<span data-ttu-id="22e12-112">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="22e12-112">ABORT_XP_HEADER_OPERATION</span></span> 
  
> <span data-ttu-id="22e12-113">El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="22e12-113">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> <span data-ttu-id="22e12-114">El proveedor de transporte tiene la opción de continuar trabajando en la operación o puede anular la operación y devolver MAPI_E_USER_CANCELED.</span><span class="sxs-lookup"><span data-stu-id="22e12-114">The transport provider has the option to continue working on the operation, or it can abort the operation and return MAPI_E_USER_CANCELED.</span></span> 
    
<span data-ttu-id="22e12-115">CONFIG_CHANGED</span><span class="sxs-lookup"><span data-stu-id="22e12-115">CONFIG_CHANGED</span></span> 
  
> <span data-ttu-id="22e12-116">Valida el estado de los proveedores de transporte actualmente cargados haciendo que la cola MAPI llame a su método [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) .</span><span class="sxs-lookup"><span data-stu-id="22e12-116">Validates the state of currently loaded transport providers by causing the MAPI spooler to call their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="22e12-117">Esta marca también proporciona a la cola MAPI la oportunidad de corregir errores críticos de proveedor de transporte sin obligar a las aplicaciones cliente a cerrar sesión y volver a iniciar la sesión.</span><span class="sxs-lookup"><span data-stu-id="22e12-117">This flag also provides the MAPI spooler an opportunity to correct critical transport-provider failures without forcing client applications to log off and then log on again.</span></span> 
    
<span data-ttu-id="22e12-118">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="22e12-118">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="22e12-119">El usuario seleccionó una operación de conexión.</span><span class="sxs-lookup"><span data-stu-id="22e12-119">The user selected a connect operation.</span></span> <span data-ttu-id="22e12-120">Cuando se usa este indicador con la marca REFRESH_XP_HEADER_CACHE o PROCESS_XP_HEADER_CACHE, la acción de conexión se produce sin almacenamiento en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="22e12-120">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the connect action occurs without caching.</span></span>
    
<span data-ttu-id="22e12-121">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="22e12-121">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="22e12-122">El usuario ha seleccionado una operación de desconexión.</span><span class="sxs-lookup"><span data-stu-id="22e12-122">The user selected a disconnect operation.</span></span> <span data-ttu-id="22e12-123">Cuando se usa este indicador con REFRESH_XP_HEADER_CACHE o PROCESS_XP_HEADER_CACHE, la acción de desconexión se produce sin almacenamiento en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="22e12-123">When this flag is used with REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE, the disconnect action occurs without caching.</span></span>
    
<span data-ttu-id="22e12-124">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="22e12-124">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="22e12-125">Las entradas de la tabla de caché de encabezado deben ser procesadas, se deben descargar todos los mensajes marcados con la marca MSGSTATUS_REMOTE_DOWNLOAD y se eliminarán todos los mensajes marcados con la marca MSGSTATUS_REMOTE_DELETE.</span><span class="sxs-lookup"><span data-stu-id="22e12-125">Entries in the header cache table should be processed, all messages marked with the MSGSTATUS_REMOTE_DOWNLOAD flag should be downloaded, and all messages marked with the MSGSTATUS_REMOTE_DELETE flag should be deleted.</span></span> <span data-ttu-id="22e12-126">Se deben mover los mensajes que tienen el conjunto MSGSTATUS_REMOTE_DOWNLOAD y MSGSTATUS_REMOTE_DELETE.</span><span class="sxs-lookup"><span data-stu-id="22e12-126">Messages that have both MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE set should be moved.</span></span>
    
<span data-ttu-id="22e12-127">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="22e12-127">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="22e12-128">Se debe descargar una nueva lista de encabezados de mensaje y se deben borrar todas las marcas de marcado del estado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="22e12-128">A new list of message headers should be downloaded, and all message status marking flags should be cleared.</span></span>
    
<span data-ttu-id="22e12-129">SUPPRESS_UI</span><span class="sxs-lookup"><span data-stu-id="22e12-129">SUPPRESS_UI</span></span> 
  
> <span data-ttu-id="22e12-130">Impide que el proveedor de transporte muestre una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="22e12-130">Prevents the transport provider from displaying a user interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="22e12-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22e12-131">Return value</span></span>

<span data-ttu-id="22e12-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="22e12-132">S_OK</span></span> 
  
> <span data-ttu-id="22e12-133">La llamada se ha realizado correctamente y ha devuelto el valor o los valores esperados.</span><span class="sxs-lookup"><span data-stu-id="22e12-133">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="22e12-134">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="22e12-134">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="22e12-135">Hay otra operación en curso; se debe permitir que se complete o debe detenerse antes de que se intente realizar esta operación.</span><span class="sxs-lookup"><span data-stu-id="22e12-135">Another operation is in progress; it should be allowed to complete, or it should be stopped before this operation is attempted.</span></span>
    
<span data-ttu-id="22e12-136">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="22e12-136">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="22e12-137">El proveedor de transporte remoto implicado no es compatible con una interfaz de usuario y la propia aplicación cliente debe mostrar el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="22e12-137">The remote transport provider involved does not support a user interface, and the client application itself should display the dialog box.</span></span>
    
<span data-ttu-id="22e12-138">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="22e12-138">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="22e12-139">El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="22e12-139">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="22e12-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="22e12-140">Remarks</span></span>

<span data-ttu-id="22e12-141">La cola MAPI llama al método **IXPLogon:: ValidateState** para admitir llamadas al método [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) para el objeto status.</span><span class="sxs-lookup"><span data-stu-id="22e12-141">The MAPI spooler calls the **IXPLogon::ValidateState** method to support calls to the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method for the status object.</span></span> <span data-ttu-id="22e12-142">El proveedor de transporte debe responder a la llamada de **IXPLogon:: ValidateState** exactamente como si la cola MAPI hubiera abierto un objeto de estado para la sesión de inicio de sesión actual y, a continuación, llamó a **IMAPIStatus:: ValidateState** en ese objeto.</span><span class="sxs-lookup"><span data-stu-id="22e12-142">The transport provider should respond to the **IXPLogon::ValidateState** call exactly as if the MAPI spooler had opened a status object for the current logon session and then called **IMAPIStatus::ValidateState** on that object.</span></span> 
  
<span data-ttu-id="22e12-143">Para admitir su implementación de **IMAPIStatus:: ValidateState**, la cola MAPI llama a **IXPLogon:: ValidateState** en todos los objetos de inicio de sesión para todos los proveedores de transporte activos que se ejecutan en una sesión de perfil.</span><span class="sxs-lookup"><span data-stu-id="22e12-143">To support its implementation of **IMAPIStatus::ValidateState**, the MAPI spooler calls **IXPLogon::ValidateState** on all logon objects for all active transport providers that are running in a profile session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="22e12-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="22e12-144">See also</span></span>



[<span data-ttu-id="22e12-145">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="22e12-145">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="22e12-146">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="22e12-146">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="22e12-147">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="22e12-147">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

