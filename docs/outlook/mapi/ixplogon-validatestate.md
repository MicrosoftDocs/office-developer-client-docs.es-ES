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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439488"
---
# <a name="ixplogonvalidatestate"></a><span data-ttu-id="4fcf0-103">IXPLogon::ValidateState</span><span class="sxs-lookup"><span data-stu-id="4fcf0-103">IXPLogon::ValidateState</span></span>

  
  
<span data-ttu-id="4fcf0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4fcf0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4fcf0-105">Comprueba el estado externo del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-105">Checks the transport provider's external status.</span></span> 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="4fcf0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4fcf0-106">Parameters</span></span>

 <span data-ttu-id="4fcf0-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="4fcf0-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="4fcf0-108">[entrada] Identificador de la ventana principal de los cuadros de diálogo o ventanas que muestra este método.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="4fcf0-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4fcf0-109">_ulFlags_</span></span>
  
> <span data-ttu-id="4fcf0-110">[entrada] Máscara de bits de marcas que controla cómo se realiza la comprobación de estado y los resultados de la comprobación de estado.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-110">[in] A bitmask of flags that controls how the status check is performed and the results of the status check.</span></span> <span data-ttu-id="4fcf0-111">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="4fcf0-111">The following flags can be set:</span></span>
    
<span data-ttu-id="4fcf0-112">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="4fcf0-112">ABORT_XP_HEADER_OPERATION</span></span> 
  
> <span data-ttu-id="4fcf0-113">El usuario canceló la operación, normalmente haciendo clic en el **botón** Cancelar de un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-113">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> <span data-ttu-id="4fcf0-114">El proveedor de transporte tiene la opción de continuar trabajando en la operación o puede anular la operación y devolver MAPI_E_USER_CANCELED.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-114">The transport provider has the option to continue working on the operation, or it can abort the operation and return MAPI_E_USER_CANCELED.</span></span> 
    
<span data-ttu-id="4fcf0-115">CONFIG_CHANGED</span><span class="sxs-lookup"><span data-stu-id="4fcf0-115">CONFIG_CHANGED</span></span> 
  
> <span data-ttu-id="4fcf0-116">Valida el estado de los proveedores de transporte cargados actualmente haciendo que la cola MAPI llame a su [método IXPLogon::AddressTypes.](ixplogon-addresstypes.md)</span><span class="sxs-lookup"><span data-stu-id="4fcf0-116">Validates the state of currently loaded transport providers by causing the MAPI spooler to call their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="4fcf0-117">Esta marca también proporciona a la cola MAPI una oportunidad para corregir errores críticos del proveedor de transporte sin forzar que las aplicaciones cliente cierren sesión y vuelvan a iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-117">This flag also provides the MAPI spooler an opportunity to correct critical transport-provider failures without forcing client applications to log off and then log on again.</span></span> 
    
<span data-ttu-id="4fcf0-118">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="4fcf0-118">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="4fcf0-119">El usuario seleccionó una operación de conexión.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-119">The user selected a connect operation.</span></span> <span data-ttu-id="4fcf0-120">Cuando esta marca se usa con la marca REFRESH_XP_HEADER_CACHE o PROCESS_XP_HEADER_CACHE, la acción de conexión se produce sin almacenamiento en caché.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-120">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the connect action occurs without caching.</span></span>
    
<span data-ttu-id="4fcf0-121">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="4fcf0-121">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="4fcf0-122">El usuario seleccionó una operación de desconexión.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-122">The user selected a disconnect operation.</span></span> <span data-ttu-id="4fcf0-123">Cuando esta marca se usa con REFRESH_XP_HEADER_CACHE o PROCESS_XP_HEADER_CACHE, la acción de desconexión se produce sin almacenamiento en caché.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-123">When this flag is used with REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE, the disconnect action occurs without caching.</span></span>
    
<span data-ttu-id="4fcf0-124">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="4fcf0-124">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="4fcf0-125">Las entradas de la tabla de caché de encabezados deben procesarse, se deben descargar todos los mensajes marcados con la marca MSGSTATUS_REMOTE_DOWNLOAD y todos los mensajes marcados con la marca MSGSTATUS_REMOTE_DELETE deben eliminarse.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-125">Entries in the header cache table should be processed, all messages marked with the MSGSTATUS_REMOTE_DOWNLOAD flag should be downloaded, and all messages marked with the MSGSTATUS_REMOTE_DELETE flag should be deleted.</span></span> <span data-ttu-id="4fcf0-126">Los mensajes que tienen MSGSTATUS_REMOTE_DOWNLOAD y MSGSTATUS_REMOTE_DELETE deben moverse.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-126">Messages that have both MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE set should be moved.</span></span>
    
<span data-ttu-id="4fcf0-127">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="4fcf0-127">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="4fcf0-128">Se debe descargar una nueva lista de encabezados de mensaje y deben borrarse todas las marcas de marcado de estado de mensaje.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-128">A new list of message headers should be downloaded, and all message status marking flags should be cleared.</span></span>
    
<span data-ttu-id="4fcf0-129">SUPPRESS_UI</span><span class="sxs-lookup"><span data-stu-id="4fcf0-129">SUPPRESS_UI</span></span> 
  
> <span data-ttu-id="4fcf0-130">Impide que el proveedor de transporte muestre una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-130">Prevents the transport provider from displaying a user interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4fcf0-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4fcf0-131">Return value</span></span>

<span data-ttu-id="4fcf0-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="4fcf0-132">S_OK</span></span> 
  
> <span data-ttu-id="4fcf0-133">La llamada se realiza correctamente y devuelve el valor o los valores esperados.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-133">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="4fcf0-134">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="4fcf0-134">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="4fcf0-135">Hay otra operación en curso; debe poder completarse o debe detenerse antes de intentar esta operación.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-135">Another operation is in progress; it should be allowed to complete, or it should be stopped before this operation is attempted.</span></span>
    
<span data-ttu-id="4fcf0-136">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="4fcf0-136">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="4fcf0-137">El proveedor de transporte remoto implicado no admite una interfaz de usuario y la propia aplicación cliente debe mostrar el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-137">The remote transport provider involved does not support a user interface, and the client application itself should display the dialog box.</span></span>
    
<span data-ttu-id="4fcf0-138">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="4fcf0-138">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="4fcf0-139">El usuario canceló la operación, normalmente haciendo clic en el **botón** Cancelar de un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-139">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4fcf0-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4fcf0-140">Remarks</span></span>

<span data-ttu-id="4fcf0-141">La cola MAPI llama al método **IXPLogon::ValidateState** para admitir llamadas al método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) para el objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-141">The MAPI spooler calls the **IXPLogon::ValidateState** method to support calls to the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method for the status object.</span></span> <span data-ttu-id="4fcf0-142">El proveedor de transporte debe responder a la llamada **IXPLogon::ValidateState** exactamente como si la cola MAPI hubiera abierto un objeto de estado para la sesión de inicio de sesión actual y, a continuación, llamara **IMAPIStatus::ValidateState** en ese objeto.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-142">The transport provider should respond to the **IXPLogon::ValidateState** call exactly as if the MAPI spooler had opened a status object for the current logon session and then called **IMAPIStatus::ValidateState** on that object.</span></span> 
  
<span data-ttu-id="4fcf0-143">Para admitir su implementación de **IMAPIStatus::ValidateState**, la cola MAPI llama a **IXPLogon::ValidateState** en todos los objetos de inicio de sesión de todos los proveedores de transporte activos que se ejecutan en una sesión de perfil.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-143">To support its implementation of **IMAPIStatus::ValidateState**, the MAPI spooler calls **IXPLogon::ValidateState** on all logon objects for all active transport providers that are running in a profile session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4fcf0-144">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4fcf0-144">See also</span></span>



[<span data-ttu-id="4fcf0-145">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="4fcf0-145">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="4fcf0-146">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="4fcf0-146">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="4fcf0-147">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4fcf0-147">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

