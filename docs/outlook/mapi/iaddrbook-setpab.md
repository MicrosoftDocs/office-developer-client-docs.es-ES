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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287017"
---
# <a name="iaddrbooksetpab"></a><span data-ttu-id="4e626-103">IAddrBook::SetPAB</span><span class="sxs-lookup"><span data-stu-id="4e626-103">IAddrBook::SetPAB</span></span>

  
  
<span data-ttu-id="4e626-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e626-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e626-105">Designa un contenedor determinado como la libreta personal de direcciones (PAB).</span><span class="sxs-lookup"><span data-stu-id="4e626-105">Designates a particular container as the personal address book (PAB).</span></span>
  
```cpp
HRESULT SetPAB(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="4e626-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="4e626-106">Parameters</span></span>

 <span data-ttu-id="4e626-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="4e626-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="4e626-108">a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="4e626-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="4e626-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="4e626-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="4e626-110">a Un puntero al identificador de entrada del contenedor que se va a designar como PAB.</span><span class="sxs-lookup"><span data-stu-id="4e626-110">[in] A pointer to the entry identifier of the container to be designated as the PAB.</span></span> <span data-ttu-id="4e626-111">El parámetro _lpEntryID_ no puede ser nulo.</span><span class="sxs-lookup"><span data-stu-id="4e626-111">The  _lpEntryID_ parameter cannot be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4e626-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4e626-112">Return value</span></span>

<span data-ttu-id="4e626-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="4e626-113">S_OK</span></span> 
  
> <span data-ttu-id="4e626-114">Se ha establecido el contenedor especificado como la PAB.</span><span class="sxs-lookup"><span data-stu-id="4e626-114">The specified container has been established as the PAB.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4e626-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4e626-115">Remarks</span></span>

<span data-ttu-id="4e626-116">Los clientes y los proveedores de servicios llaman al método **SetPAB** para designar un contenedor concreto como PAB.</span><span class="sxs-lookup"><span data-stu-id="4e626-116">Clients and service providers call the **SetPAB** method to designate a particular container as the PAB.</span></span> <span data-ttu-id="4e626-117">La PAB es un contenedor que consta de entradas copiadas de otros contenedores, así como nuevas entradas.</span><span class="sxs-lookup"><span data-stu-id="4e626-117">The PAB is a container that consists of entries copied from other containers as well as new entries.</span></span> 
  
<span data-ttu-id="4e626-118">Una llamada a **SetPAB** establece un contenedor como PAB hasta que no está disponible o un nuevo contenedor se convierte en la PAB a través de una llamada subsiguiente a **SetPAB**.</span><span class="sxs-lookup"><span data-stu-id="4e626-118">A call to **SetPAB** establishes a container as the PAB until that container is made unavailable or a new container becomes the PAB through a subsequent call to **SetPAB**.</span></span> 
  
<span data-ttu-id="4e626-119">Los clientes y proveedores no tienen que llamar al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) para hacer que el cambio de PAB sea permanente.</span><span class="sxs-lookup"><span data-stu-id="4e626-119">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to make the PAB change permanent.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4e626-120">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="4e626-120">MFCMAPI reference</span></span>

<span data-ttu-id="4e626-121">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="4e626-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4e626-122">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="4e626-122">**File**</span></span>|<span data-ttu-id="4e626-123">**Función**</span><span class="sxs-lookup"><span data-stu-id="4e626-123">**Function**</span></span>|<span data-ttu-id="4e626-124">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="4e626-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4e626-125">AbContDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="4e626-125">AbContDlg.cpp</span></span>  <br/> |<span data-ttu-id="4e626-126">CAbContDlg:: OnSetPAB</span><span class="sxs-lookup"><span data-stu-id="4e626-126">CAbContDlg::OnSetPAB</span></span>  <br/> |<span data-ttu-id="4e626-127">MFCMAPI usa el método **SetPAB** para convertir el contenedor especificado en la PAB.</span><span class="sxs-lookup"><span data-stu-id="4e626-127">MFCMAPI uses the **SetPAB** method to make the specified container the PAB.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4e626-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e626-128">See also</span></span>



[<span data-ttu-id="4e626-129">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="4e626-129">IAddrBook::GetPAB</span></span>](iaddrbook-getpab.md)
  
[<span data-ttu-id="4e626-130">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="4e626-130">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="4e626-131">Propiedad canónica PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="4e626-131">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="4e626-132">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4e626-132">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="4e626-133">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="4e626-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

