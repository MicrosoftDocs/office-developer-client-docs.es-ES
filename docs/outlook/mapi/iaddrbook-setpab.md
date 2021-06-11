---
title: IAddrBookSetPAB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetPAB
api_type:
- COM
ms.assetid: 75daf9d4-6975-435f-91e5-1b41e0047ab7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 29677ce74f405e8ca03f1639f3d98288532e9653
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424619"
---
# <a name="iaddrbooksetpab"></a><span data-ttu-id="ac943-103">IAddrBook::SetPAB</span><span class="sxs-lookup"><span data-stu-id="ac943-103">IAddrBook::SetPAB</span></span>

  
  
<span data-ttu-id="ac943-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac943-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac943-105">Designa un contenedor concreto como la libreta de direcciones personal (PAB).</span><span class="sxs-lookup"><span data-stu-id="ac943-105">Designates a particular container as the personal address book (PAB).</span></span>
  
```cpp
HRESULT SetPAB(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="ac943-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="ac943-106">Parameters</span></span>

 <span data-ttu-id="ac943-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="ac943-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="ac943-108">[in] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="ac943-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="ac943-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="ac943-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="ac943-110">[in] Puntero al identificador de entrada del contenedor que se designará como PAB.</span><span class="sxs-lookup"><span data-stu-id="ac943-110">[in] A pointer to the entry identifier of the container to be designated as the PAB.</span></span> <span data-ttu-id="ac943-111">El  _parámetro lpEntryID_ no puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="ac943-111">The  _lpEntryID_ parameter cannot be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ac943-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ac943-112">Return value</span></span>

<span data-ttu-id="ac943-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="ac943-113">S_OK</span></span> 
  
> <span data-ttu-id="ac943-114">El contenedor especificado se ha establecido como PAB.</span><span class="sxs-lookup"><span data-stu-id="ac943-114">The specified container has been established as the PAB.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ac943-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ac943-115">Remarks</span></span>

<span data-ttu-id="ac943-116">Los clientes y proveedores de servicios llaman al **método SetPAB** para designar un contenedor determinado como PAB.</span><span class="sxs-lookup"><span data-stu-id="ac943-116">Clients and service providers call the **SetPAB** method to designate a particular container as the PAB.</span></span> <span data-ttu-id="ac943-117">El PAB es un contenedor que consta de entradas copiadas de otros contenedores, así como entradas nuevas.</span><span class="sxs-lookup"><span data-stu-id="ac943-117">The PAB is a container that consists of entries copied from other containers as well as new entries.</span></span> 
  
<span data-ttu-id="ac943-118">Una llamada a **SetPAB** establece un contenedor como PAB hasta que dicho contenedor no está disponible o un nuevo contenedor se convierte en el PAB a través de una llamada posterior a **SetPAB**.</span><span class="sxs-lookup"><span data-stu-id="ac943-118">A call to **SetPAB** establishes a container as the PAB until that container is made unavailable or a new container becomes the PAB through a subsequent call to **SetPAB**.</span></span> 
  
<span data-ttu-id="ac943-119">Los clientes y proveedores no tienen que llamar al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para que el cambio de PAB sea permanente.</span><span class="sxs-lookup"><span data-stu-id="ac943-119">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to make the PAB change permanent.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ac943-120">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ac943-120">MFCMAPI reference</span></span>

<span data-ttu-id="ac943-121">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="ac943-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ac943-122">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="ac943-122">**File**</span></span>|<span data-ttu-id="ac943-123">**Función**</span><span class="sxs-lookup"><span data-stu-id="ac943-123">**Function**</span></span>|<span data-ttu-id="ac943-124">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="ac943-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ac943-125">AbContDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="ac943-125">AbContDlg.cpp</span></span>  <br/> |<span data-ttu-id="ac943-126">CAbContDlg::OnSetPAB</span><span class="sxs-lookup"><span data-stu-id="ac943-126">CAbContDlg::OnSetPAB</span></span>  <br/> |<span data-ttu-id="ac943-127">MFCMAPI usa el **método SetPAB** para convertir el contenedor especificado en PAB.</span><span class="sxs-lookup"><span data-stu-id="ac943-127">MFCMAPI uses the **SetPAB** method to make the specified container the PAB.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ac943-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac943-128">See also</span></span>



[<span data-ttu-id="ac943-129">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="ac943-129">IAddrBook::GetPAB</span></span>](iaddrbook-getpab.md)
  
[<span data-ttu-id="ac943-130">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="ac943-130">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="ac943-131">Propiedad canónica PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="ac943-131">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="ac943-132">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ac943-132">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="ac943-133">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="ac943-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

