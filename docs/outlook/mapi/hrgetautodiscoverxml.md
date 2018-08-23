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
ms.openlocfilehash: 490c834ee63c158b3f9c0e34f8de7f582c650bc4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584068"
---
# <a name="hrgetautodiscoverxml"></a><span data-ttu-id="e7b36-103">HrGetAutoDiscoverXML</span><span class="sxs-lookup"><span data-stu-id="e7b36-103">HrGetAutoDiscoverXML</span></span>

  
  
<span data-ttu-id="e7b36-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7b36-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7b36-105">Devuelve una secuencia de lenguaje de marcado Extensible (XML) que representa información recuperada desde el servicio de detección automática de un servidor de Microsoft Exchange 2007.</span><span class="sxs-lookup"><span data-stu-id="e7b36-105">Returns an Extensible Markup Language (XML) stream that represents information retrieved from the auto-discovery service of a Microsoft Exchange 2007 server.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e7b36-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="e7b36-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e7b36-107">Exportada por:</span><span class="sxs-lookup"><span data-stu-id="e7b36-107">Exported by:</span></span>  <br/> |<span data-ttu-id="e7b36-108">olmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="e7b36-108">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="e7b36-109">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="e7b36-109">Called by:</span></span>  <br/> |<span data-ttu-id="e7b36-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="e7b36-110">Client</span></span>  <br/> |
|<span data-ttu-id="e7b36-111">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="e7b36-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="e7b36-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="e7b36-112">Outlook</span></span>  <br/> |
   
```cpp
HRESULT HrGetAutoDiscoverXML( 
    __in_z const WCHAR *pwzAddress, 
    __in_opt_z const WCHAR *pwzPassword, 
    __in_opt HANDLE hCancelEvent, 
    __in_opt ULONG ulFlags, 
    __out IStream** ppXmlStream); 

```

## <a name="parameters"></a><span data-ttu-id="e7b36-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e7b36-113">Parameters</span></span>

 <span data-ttu-id="e7b36-114">_pwzAddress_</span><span class="sxs-lookup"><span data-stu-id="e7b36-114">_pwzAddress_</span></span>
  
> <span data-ttu-id="e7b36-115">[entrada] Una terminada en null Protocolo Simple de transferencia de correo (SMTP) dirección de correo electrónico de la cuenta para la que desea recuperar la información de detección automática.</span><span class="sxs-lookup"><span data-stu-id="e7b36-115">[in] A null-terminated Simple Mail Transfer Protocol (SMTP) email address of the account for which you want to retrieve the auto-discovery information.</span></span>
    
 <span data-ttu-id="e7b36-116">_pwzPassword_</span><span class="sxs-lookup"><span data-stu-id="e7b36-116">_pwzPassword_</span></span>
  
> <span data-ttu-id="e7b36-117">[entrada] Una contraseña opcional para la cuenta especificada por _pwzAddress_.</span><span class="sxs-lookup"><span data-stu-id="e7b36-117">[in] An optional password for the account specified by  _pwzAddress_.</span></span> <span data-ttu-id="e7b36-118">Tenga en cuenta que pasar cualquier contraseña no tiene ningún efecto si la cuenta especificada por _pwzAddress_ no requiere una contraseña.</span><span class="sxs-lookup"><span data-stu-id="e7b36-118">Note that passing any password has no effect if the account specified by  _pwzAddress_ does not require a password.</span></span> 
    
 <span data-ttu-id="e7b36-119">_hCancelEvent_</span><span class="sxs-lookup"><span data-stu-id="e7b36-119">_hCancelEvent_</span></span>
  
> <span data-ttu-id="e7b36-120">[entrada] Un identificador de evento de Win32 no establecido al que es opcional y se puede usar para cancelar la operación.</span><span class="sxs-lookup"><span data-stu-id="e7b36-120">[in] An unset Win32 event handle that is optional and can be used to cancel the operation.</span></span> <span data-ttu-id="e7b36-121">Para cancelar la operación, establezca el evento y pase el identificador de evento como _hCancelEvent_; pase **null** si no desea cancelar la operación.</span><span class="sxs-lookup"><span data-stu-id="e7b36-121">To cancel the operation, set the event and pass the event handle as  _hCancelEvent_; pass **null** if you do not want to cancel the operation.</span></span> <span data-ttu-id="e7b36-122">Tenga en cuenta que si se pasa un valor que no representa un identificador de evento no tiene ningún efecto y se omite por la función.</span><span class="sxs-lookup"><span data-stu-id="e7b36-122">Note that passing a value that does not represent an event handle has no effect and is ignored by the function.</span></span> 
    
 <span data-ttu-id="e7b36-123">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e7b36-123">_ulFlags_</span></span>
  
> <span data-ttu-id="e7b36-124">[entrada] Este parámetro no se usa.</span><span class="sxs-lookup"><span data-stu-id="e7b36-124">[in] This parameter is not used.</span></span> <span data-ttu-id="e7b36-125">Debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="e7b36-125">It must be 0.</span></span>
    
 <span data-ttu-id="e7b36-126">_ppXmlStream_</span><span class="sxs-lookup"><span data-stu-id="e7b36-126">_ppXmlStream_</span></span>
  
> <span data-ttu-id="e7b36-127">[out] Un puntero a un objeto [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) que contiene el XML de detección automática.</span><span class="sxs-lookup"><span data-stu-id="e7b36-127">[out] A pointer to an [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) object that contains the autodiscovery XML.</span></span> <span data-ttu-id="e7b36-128">Devuelve **null** si se produce un error en la operación de detección automática.</span><span class="sxs-lookup"><span data-stu-id="e7b36-128">Returns **null** if the autodiscovery operation fails.</span></span> <span data-ttu-id="e7b36-129">Debe liberar el objeto [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) cuando haya terminado con él.</span><span class="sxs-lookup"><span data-stu-id="e7b36-129">You must release the [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) object when you are finished with it.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="e7b36-130">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="e7b36-130">Return values</span></span>

<span data-ttu-id="e7b36-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="e7b36-131">S_OK</span></span> 
  
- <span data-ttu-id="e7b36-132">La llamada a la función es correcta.</span><span class="sxs-lookup"><span data-stu-id="e7b36-132">The function call is successful.</span></span>
    
<span data-ttu-id="e7b36-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="e7b36-133">E_INVALIDARG</span></span> 
  
-  <span data-ttu-id="e7b36-134">_pwzAddress_ es **null** o no es una dirección SMTP válida, o _ppXmlStream_ es un puntero **nulo** a un objeto [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e7b36-134">_pwzAddress_ is **null** or is not a valid SMTP address, or  _ppXmlStream_ is a **null** pointer to an [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) object.</span></span> 
    
<span data-ttu-id="e7b36-135">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="e7b36-135">MAPI_E_NOT_FOUND</span></span> 
  
- <span data-ttu-id="e7b36-136">Equipo cliente no está conectado a la red, equipo cliente no está conectado a un servidor de Microsoft Exchange 2007, _pwzAddress_ no es una cuenta en un servidor de Exchange 2007 o _pwzAddress_ es una cuenta que no es compatible con Exchange servicio de detección automática.</span><span class="sxs-lookup"><span data-stu-id="e7b36-136">Client computer is not connected to the network, client computer is not connected to a Microsoft Exchange 2007 server,  _pwzAddress_ is not an account on an Exchange 2007 server, or  _pwzAddress_ is an account that does not support Exchange auto-discovery service.</span></span> 
    
<span data-ttu-id="e7b36-137">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="e7b36-137">MAPI_E_USER_CANCEL</span></span> 
  
- <span data-ttu-id="e7b36-138">Se ha pasado un identificador de evento a _hCancelEvent_ para cancelar la operación.</span><span class="sxs-lookup"><span data-stu-id="e7b36-138">An event handle has been passed to  _hCancelEvent_ to cancel the operation.</span></span> 
    
<span data-ttu-id="e7b36-139">STRSAFE_E_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="e7b36-139">STRSAFE_E_INSUFFICIENT_BUFFER</span></span>
  
- <span data-ttu-id="e7b36-140">El valor pasado a _pwzAddress_ o _pwzPassword_ es demasiado largo, por ejemplo, que desborda el búfer interno de tamaño de 256 bytes.</span><span class="sxs-lookup"><span data-stu-id="e7b36-140">The value passed to  _pwzAddress_ or  _pwzPassword_ is too long, such that it overflows the internal buffer of size 256 bytes.</span></span> 
    

