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
ms.openlocfilehash: 3f13a4d278b85ffae33e8f44f3a15eb499fb11b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817154"
---
# <a name="iaddrbooksetpab"></a><span data-ttu-id="dc6c7-103">IAddrBook::SetPAB</span><span class="sxs-lookup"><span data-stu-id="dc6c7-103">IAddrBook::SetPAB</span></span>

  
  
<span data-ttu-id="dc6c7-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dc6c7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dc6c7-105">Designa un contenedor determinado como la libreta de direcciones personales (PAB).</span><span class="sxs-lookup"><span data-stu-id="dc6c7-105">Designates a particular container as the personal address book (PAB).</span></span>
  
```cpp
HRESULT SetPAB(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="dc6c7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dc6c7-106">Parameters</span></span>

 <span data-ttu-id="dc6c7-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="dc6c7-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="dc6c7-108">[entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="dc6c7-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="dc6c7-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="dc6c7-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="dc6c7-110">[entrada] Un puntero al identificador de entrada del contenedor que se designarán como el archivo PAB.</span><span class="sxs-lookup"><span data-stu-id="dc6c7-110">[in] A pointer to the entry identifier of the container to be designated as the PAB.</span></span> <span data-ttu-id="dc6c7-111">El parámetro _lpEntryID_ no puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="dc6c7-111">The  _lpEntryID_ parameter cannot be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dc6c7-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc6c7-112">Return value</span></span>

<span data-ttu-id="dc6c7-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="dc6c7-113">S_OK</span></span> 
  
> <span data-ttu-id="dc6c7-114">El contenedor especificado se ha establecido como el archivo PAB.</span><span class="sxs-lookup"><span data-stu-id="dc6c7-114">The specified container has been established as the PAB.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dc6c7-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dc6c7-115">Remarks</span></span>

<span data-ttu-id="dc6c7-116">Los clientes y proveedores de servicios de llamar al método **SetPAB** para designar un contenedor determinado como el archivo PAB.</span><span class="sxs-lookup"><span data-stu-id="dc6c7-116">Clients and service providers call the **SetPAB** method to designate a particular container as the PAB.</span></span> <span data-ttu-id="dc6c7-117">El archivo PAB es un contenedor que consta de las entradas que se copió desde otros contenedores, así como las nuevas entradas.</span><span class="sxs-lookup"><span data-stu-id="dc6c7-117">The PAB is a container that consists of entries copied from other containers as well as new entries.</span></span> 
  
<span data-ttu-id="dc6c7-118">Una llamada a **SetPAB** establece un contenedor como el archivo PAB hasta que ese contenedor se realiza no está disponible o un contenedor nuevo se convierte en la Libreta personal de direcciones a través de una llamada posterior a **SetPAB**.</span><span class="sxs-lookup"><span data-stu-id="dc6c7-118">A call to **SetPAB** establishes a container as the PAB until that container is made unavailable or a new container becomes the PAB through a subsequent call to **SetPAB**.</span></span> 
  
<span data-ttu-id="dc6c7-119">Los clientes y proveedores no es necesario que llamar al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para que el cambio PAB sea permanente.</span><span class="sxs-lookup"><span data-stu-id="dc6c7-119">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to make the PAB change permanent.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="dc6c7-120">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="dc6c7-120">MFCMAPI reference</span></span>

<span data-ttu-id="dc6c7-121">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="dc6c7-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="dc6c7-122">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="dc6c7-122">**File**</span></span>|<span data-ttu-id="dc6c7-123">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="dc6c7-123">**Function**</span></span>|<span data-ttu-id="dc6c7-124">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="dc6c7-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dc6c7-125">AbContDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="dc6c7-125">AbContDlg.cpp</span></span>  <br/> |<span data-ttu-id="dc6c7-126">CAbContDlg::OnSetPAB</span><span class="sxs-lookup"><span data-stu-id="dc6c7-126">CAbContDlg::OnSetPAB</span></span>  <br/> |<span data-ttu-id="dc6c7-127">MFCMAPI, utiliza el método **SetPAB** para realizar el contenedor especificado de la Libreta personal de direcciones.</span><span class="sxs-lookup"><span data-stu-id="dc6c7-127">MFCMAPI uses the **SetPAB** method to make the specified container the PAB.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dc6c7-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc6c7-128">See also</span></span>



[<span data-ttu-id="dc6c7-129">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="dc6c7-129">IAddrBook::GetPAB</span></span>](iaddrbook-getpab.md)
  
[<span data-ttu-id="dc6c7-130">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="dc6c7-130">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="dc6c7-131">Propiedad canónica PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="dc6c7-131">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="dc6c7-132">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="dc6c7-132">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="dc6c7-133">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="dc6c7-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

