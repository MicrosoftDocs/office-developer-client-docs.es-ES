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
ms.openlocfilehash: 4fd0dd02c5cf6f6a49b782d06c02e373dcfc3327
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577488"
---
# <a name="ixplogonvalidatestate"></a><span data-ttu-id="cc695-103">IXPLogon::ValidateState</span><span class="sxs-lookup"><span data-stu-id="cc695-103">IXPLogon::ValidateState</span></span>

  
  
<span data-ttu-id="cc695-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc695-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc695-105">Comprobaciones de estado externo del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="cc695-105">Checks the transport provider's external status.</span></span> 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="cc695-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cc695-106">Parameters</span></span>

 <span data-ttu-id="cc695-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="cc695-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="cc695-108">[entrada] Identificador de la ventana principal de los cuadros de diálogo o windows que muestra este método.</span><span class="sxs-lookup"><span data-stu-id="cc695-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="cc695-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cc695-109">_ulFlags_</span></span>
  
> <span data-ttu-id="cc695-110">[entrada] Una máscara de bits de indicadores que controla cómo se realiza la comprobación de estado y los resultados de la comprobación de estado.</span><span class="sxs-lookup"><span data-stu-id="cc695-110">[in] A bitmask of flags that controls how the status check is performed and the results of the status check.</span></span> <span data-ttu-id="cc695-111">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="cc695-111">The following flags can be set:</span></span>
    
<span data-ttu-id="cc695-112">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="cc695-112">ABORT_XP_HEADER_OPERATION</span></span> 
  
> <span data-ttu-id="cc695-113">El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="cc695-113">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> <span data-ttu-id="cc695-114">El proveedor de transporte tiene la opción para continuar trabajando en la operación, o se puede anular la operación y devolver MAPI_E_USER_CANCELED.</span><span class="sxs-lookup"><span data-stu-id="cc695-114">The transport provider has the option to continue working on the operation, or it can abort the operation and return MAPI_E_USER_CANCELED.</span></span> 
    
<span data-ttu-id="cc695-115">CONFIG_CHANGED</span><span class="sxs-lookup"><span data-stu-id="cc695-115">CONFIG_CHANGED</span></span> 
  
> <span data-ttu-id="cc695-116">Valida el estado de los proveedores de transporte actualmente cargados por lo que provoca que la cola MAPI llamar a su método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) .</span><span class="sxs-lookup"><span data-stu-id="cc695-116">Validates the state of currently loaded transport providers by causing the MAPI spooler to call their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="cc695-117">Esta marca también proporciona una oportunidad para corregir errores críticos del proveedor de transporte sin necesidad de aplicaciones de cliente para cerrar sesión y, a continuación, vuelva a iniciar sesión de la cola de MAPI.</span><span class="sxs-lookup"><span data-stu-id="cc695-117">This flag also provides the MAPI spooler an opportunity to correct critical transport-provider failures without forcing client applications to log off and then log on again.</span></span> 
    
<span data-ttu-id="cc695-118">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="cc695-118">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="cc695-119">El usuario ha seleccionado una operación de conexión.</span><span class="sxs-lookup"><span data-stu-id="cc695-119">The user selected a connect operation.</span></span> <span data-ttu-id="cc695-120">Cuando este indicador se utiliza con el indicador REFRESH_XP_HEADER_CACHE o PROCESS_XP_HEADER_CACHE, se produce la acción de conexión sin almacenamiento en caché.</span><span class="sxs-lookup"><span data-stu-id="cc695-120">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the connect action occurs without caching.</span></span>
    
<span data-ttu-id="cc695-121">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="cc695-121">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="cc695-122">El usuario ha seleccionado una operación de desconexión.</span><span class="sxs-lookup"><span data-stu-id="cc695-122">The user selected a disconnect operation.</span></span> <span data-ttu-id="cc695-123">Cuando se utiliza esta marca con REFRESH_XP_HEADER_CACHE o PROCESS_XP_HEADER_CACHE, se produce la acción de desconexión sin almacenamiento en caché.</span><span class="sxs-lookup"><span data-stu-id="cc695-123">When this flag is used with REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE, the disconnect action occurs without caching.</span></span>
    
<span data-ttu-id="cc695-124">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="cc695-124">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="cc695-125">Se deben procesar las entradas de la tabla de la memoria caché de encabezado, que deben descargarse todos los mensajes marcados con la marca MSGSTATUS_REMOTE_DOWNLOAD y se deben eliminar todos los mensajes marcados con la marca MSGSTATUS_REMOTE_DELETE.</span><span class="sxs-lookup"><span data-stu-id="cc695-125">Entries in the header cache table should be processed, all messages marked with the MSGSTATUS_REMOTE_DOWNLOAD flag should be downloaded, and all messages marked with the MSGSTATUS_REMOTE_DELETE flag should be deleted.</span></span> <span data-ttu-id="cc695-126">Los mensajes que tienen MSGSTATUS_REMOTE_DOWNLOAD y MSGSTATUS_REMOTE_DELETE establecer se va a mover.</span><span class="sxs-lookup"><span data-stu-id="cc695-126">Messages that have both MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE set should be moved.</span></span>
    
<span data-ttu-id="cc695-127">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="cc695-127">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="cc695-128">Una nueva lista de encabezados de mensaje que debe descargarse y se debe borrar el estado del mensaje todos los indicadores de marcadores.</span><span class="sxs-lookup"><span data-stu-id="cc695-128">A new list of message headers should be downloaded, and all message status marking flags should be cleared.</span></span>
    
<span data-ttu-id="cc695-129">SUPPRESS_UI</span><span class="sxs-lookup"><span data-stu-id="cc695-129">SUPPRESS_UI</span></span> 
  
> <span data-ttu-id="cc695-130">Impide que el proveedor de transporte mostrar la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="cc695-130">Prevents the transport provider from displaying a user interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cc695-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cc695-131">Return value</span></span>

<span data-ttu-id="cc695-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="cc695-132">S_OK</span></span> 
  
> <span data-ttu-id="cc695-133">La llamada se ha realizado correctamente y devuelve el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="cc695-133">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="cc695-134">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="cc695-134">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="cc695-135">Otra operación está en curso; se debe permitir para llevar a cabo o se debe detener antes de intenta esta operación.</span><span class="sxs-lookup"><span data-stu-id="cc695-135">Another operation is in progress; it should be allowed to complete, or it should be stopped before this operation is attempted.</span></span>
    
<span data-ttu-id="cc695-136">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="cc695-136">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="cc695-137">El proveedor de transporte remoto implicado no es compatible con una interfaz de usuario y la propia aplicación cliente debe mostrar el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="cc695-137">The remote transport provider involved does not support a user interface, and the client application itself should display the dialog box.</span></span>
    
<span data-ttu-id="cc695-138">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="cc695-138">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="cc695-139">El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="cc695-139">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="cc695-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cc695-140">Remarks</span></span>

<span data-ttu-id="cc695-141">La cola MAPI llama el método **IXPLogon::ValidateState** para admitir las llamadas al método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) para el objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="cc695-141">The MAPI spooler calls the **IXPLogon::ValidateState** method to support calls to the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method for the status object.</span></span> <span data-ttu-id="cc695-142">El proveedor de transporte debe responder a la llamada **IXPLogon::ValidateState** exactamente como si hubiera abierto un objeto de estado para la sesión actual de inicio de sesión y, a continuación, llame **IMAPIStatus::ValidateState** en ese objeto la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="cc695-142">The transport provider should respond to the **IXPLogon::ValidateState** call exactly as if the MAPI spooler had opened a status object for the current logon session and then called **IMAPIStatus::ValidateState** on that object.</span></span> 
  
<span data-ttu-id="cc695-143">Para admitir su implementación de **IMAPIStatus::ValidateState**, la cola MAPI llama a **IXPLogon::ValidateState** en todos los objetos de inicio de sesión para todos los proveedores de transporte de activo que se ejecutan en una sesión de perfil.</span><span class="sxs-lookup"><span data-stu-id="cc695-143">To support its implementation of **IMAPIStatus::ValidateState**, the MAPI spooler calls **IXPLogon::ValidateState** on all logon objects for all active transport providers that are running in a profile session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cc695-144">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="cc695-144">See also</span></span>



[<span data-ttu-id="cc695-145">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="cc695-145">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="cc695-146">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="cc695-146">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="cc695-147">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cc695-147">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

