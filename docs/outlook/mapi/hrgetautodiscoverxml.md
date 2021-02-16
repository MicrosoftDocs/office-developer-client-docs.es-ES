---
title: HrGetAutoDiscoverXML
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrGetAutoDiscoverXML
api_type:
- COM
ms.assetid: 03691187-7c65-620b-576f-6ebe62a80830
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 77f28654ffe0f6f459fde229bb7428f2c39e96c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347806"
---
# <a name="hrgetautodiscoverxml"></a><span data-ttu-id="8dbec-103">HrGetAutoDiscoverXML</span><span class="sxs-lookup"><span data-stu-id="8dbec-103">HrGetAutoDiscoverXML</span></span>

  
  
<span data-ttu-id="8dbec-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8dbec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8dbec-105">Devuelve una secuencia de lenguaje de marcado extensible (XML) que representa la información recuperada del servicio de detección automática de un servidor de Microsoft Exchange 2007.</span><span class="sxs-lookup"><span data-stu-id="8dbec-105">Returns an Extensible Markup Language (XML) stream that represents information retrieved from the auto-discovery service of a Microsoft Exchange 2007 server.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8dbec-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="8dbec-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8dbec-107">Exportado por:</span><span class="sxs-lookup"><span data-stu-id="8dbec-107">Exported by:</span></span>  <br/> |<span data-ttu-id="8dbec-108">olmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="8dbec-108">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="8dbec-109">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="8dbec-109">Called by:</span></span>  <br/> |<span data-ttu-id="8dbec-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="8dbec-110">Client</span></span>  <br/> |
|<span data-ttu-id="8dbec-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="8dbec-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="8dbec-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="8dbec-112">Outlook</span></span>  <br/> |
   
```cpp
HRESULT HrGetAutoDiscoverXML( 
    __in_z const WCHAR *pwzAddress, 
    __in_opt_z const WCHAR *pwzPassword, 
    __in_opt HANDLE hCancelEvent, 
    __in_opt ULONG ulFlags, 
    __out IStream** ppXmlStream); 

```

## <a name="parameters"></a><span data-ttu-id="8dbec-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8dbec-113">Parameters</span></span>

 <span data-ttu-id="8dbec-114">_pwzAddress_</span><span class="sxs-lookup"><span data-stu-id="8dbec-114">_pwzAddress_</span></span>
  
> <span data-ttu-id="8dbec-115">[entrada] Una dirección de correo electrónico smtp (Protocolo simple de transferencia de correo) terminada en null de la cuenta para la que desea recuperar la información de detección automática.</span><span class="sxs-lookup"><span data-stu-id="8dbec-115">[in] A null-terminated Simple Mail Transfer Protocol (SMTP) email address of the account for which you want to retrieve the auto-discovery information.</span></span>
    
 <span data-ttu-id="8dbec-116">_pwzPassword_</span><span class="sxs-lookup"><span data-stu-id="8dbec-116">_pwzPassword_</span></span>
  
> <span data-ttu-id="8dbec-117">[entrada] Una contraseña opcional para la cuenta especificada por  _pwzAddress_.</span><span class="sxs-lookup"><span data-stu-id="8dbec-117">[in] An optional password for the account specified by  _pwzAddress_.</span></span> <span data-ttu-id="8dbec-118">Tenga en cuenta que pasar cualquier contraseña no tiene ningún efecto si la cuenta especificada por  _pwzAddress_ no requiere una contraseña.</span><span class="sxs-lookup"><span data-stu-id="8dbec-118">Note that passing any password has no effect if the account specified by  _pwzAddress_ does not require a password.</span></span> 
    
 <span data-ttu-id="8dbec-119">_hCancelEvent_</span><span class="sxs-lookup"><span data-stu-id="8dbec-119">_hCancelEvent_</span></span>
  
> <span data-ttu-id="8dbec-120">[entrada] Un identificador de evento win32 sin establecer que es opcional y se puede usar para cancelar la operación.</span><span class="sxs-lookup"><span data-stu-id="8dbec-120">[in] An unset Win32 event handle that is optional and can be used to cancel the operation.</span></span> <span data-ttu-id="8dbec-121">Para cancelar la operación, establezca el evento y pase el identificador de evento  _como hCancelEvent_; pass **null** si no desea cancelar la operación.</span><span class="sxs-lookup"><span data-stu-id="8dbec-121">To cancel the operation, set the event and pass the event handle as  _hCancelEvent_; pass **null** if you do not want to cancel the operation.</span></span> <span data-ttu-id="8dbec-122">Tenga en cuenta que pasar un valor que no representa un identificador de evento no tiene ningún efecto y la función lo omite.</span><span class="sxs-lookup"><span data-stu-id="8dbec-122">Note that passing a value that does not represent an event handle has no effect and is ignored by the function.</span></span> 
    
 <span data-ttu-id="8dbec-123">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8dbec-123">_ulFlags_</span></span>
  
> <span data-ttu-id="8dbec-124">[entrada] Este parámetro no se usa.</span><span class="sxs-lookup"><span data-stu-id="8dbec-124">[in] This parameter is not used.</span></span> <span data-ttu-id="8dbec-125">Debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="8dbec-125">It must be 0.</span></span>
    
 <span data-ttu-id="8dbec-126">_ppXmlStream_</span><span class="sxs-lookup"><span data-stu-id="8dbec-126">_ppXmlStream_</span></span>
  
> <span data-ttu-id="8dbec-127">[salida] Puntero a un [objeto IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) que contiene el XML de detección automática.</span><span class="sxs-lookup"><span data-stu-id="8dbec-127">[out] A pointer to an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object that contains the autodiscovery XML.</span></span> <span data-ttu-id="8dbec-128">Devuelve **null** si se produce un error en la operación de detección automática.</span><span class="sxs-lookup"><span data-stu-id="8dbec-128">Returns **null** if the autodiscovery operation fails.</span></span> <span data-ttu-id="8dbec-129">Debes liberar el [objeto IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) cuando termines con él.</span><span class="sxs-lookup"><span data-stu-id="8dbec-129">You must release the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object when you are finished with it.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="8dbec-130">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="8dbec-130">Return values</span></span>

<span data-ttu-id="8dbec-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="8dbec-131">S_OK</span></span> 
  
- <span data-ttu-id="8dbec-132">La llamada a la función se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="8dbec-132">The function call is successful.</span></span>
    
<span data-ttu-id="8dbec-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="8dbec-133">E_INVALIDARG</span></span> 
  
-  <span data-ttu-id="8dbec-134">_pwzAddress_ es **null** o no es una dirección SMTP válida, o _ppXmlStream_ es un puntero nulo **a** un objeto [IStream.](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8dbec-134">_pwzAddress_ is **null** or is not a valid SMTP address, or  _ppXmlStream_ is a **null** pointer to an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object.</span></span> 
    
<span data-ttu-id="8dbec-135">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="8dbec-135">MAPI_E_NOT_FOUND</span></span> 
  
- <span data-ttu-id="8dbec-136">El equipo cliente no está conectado a la red, el equipo cliente no está conectado a un servidor de Microsoft Exchange 2007,  _pwzAddress_ no es una cuenta en un servidor de Exchange 2007 o  _pwzAddress_ es una cuenta que no admite el servicio de detección automática de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8dbec-136">Client computer is not connected to the network, client computer is not connected to a Microsoft Exchange 2007 server,  _pwzAddress_ is not an account on an Exchange 2007 server, or  _pwzAddress_ is an account that does not support Exchange auto-discovery service.</span></span> 
    
<span data-ttu-id="8dbec-137">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="8dbec-137">MAPI_E_USER_CANCEL</span></span> 
  
- <span data-ttu-id="8dbec-138">Se ha pasado un identificador de evento  _a hCancelEvent_ para cancelar la operación.</span><span class="sxs-lookup"><span data-stu-id="8dbec-138">An event handle has been passed to  _hCancelEvent_ to cancel the operation.</span></span> 
    
<span data-ttu-id="8dbec-139">STRSAFE_E_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="8dbec-139">STRSAFE_E_INSUFFICIENT_BUFFER</span></span>
  
- <span data-ttu-id="8dbec-140">El valor pasado  _a pwzAddress_ o  _pwzPassword_ es demasiado largo, por lo que desborda el búfer interno de tamaño de 256 bytes.</span><span class="sxs-lookup"><span data-stu-id="8dbec-140">The value passed to  _pwzAddress_ or  _pwzPassword_ is too long, such that it overflows the internal buffer of size 256 bytes.</span></span> 
    

