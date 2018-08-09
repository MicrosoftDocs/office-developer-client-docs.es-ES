---
title: IAddrBookGetDefaultDir
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetDefaultDir
api_type:
- COM
ms.assetid: 7a9fdf3f-fd76-40fb-8217-967c6efba5f6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7309f65965fe3c88f927eeba0bbcccff97c479af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817137"
---
# <a name="iaddrbookgetdefaultdir"></a><span data-ttu-id="1d4c2-103">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="1d4c2-103">IAddrBook::GetDefaultDir</span></span>

  
  
<span data-ttu-id="1d4c2-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1d4c2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1d4c2-105">Devuelve el identificador de entrada para el contenedor de la libreta de direcciones inicial.</span><span class="sxs-lookup"><span data-stu-id="1d4c2-105">Returns the entry identifier for the initial address book container.</span></span>
  
```cpp
HRESULT GetDefaultDir(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="1d4c2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1d4c2-106">Parameters</span></span>

 <span data-ttu-id="1d4c2-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="1d4c2-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="1d4c2-108">[out] Un puntero para el número de bytes en el identificador de entrada indicado por el parámetro _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="1d4c2-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="1d4c2-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="1d4c2-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="1d4c2-110">[out] Un puntero a un puntero al identificador de entrada del contenedor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1d4c2-110">[out] A pointer to a pointer to the entry identifier of the default container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1d4c2-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1d4c2-111">Return value</span></span>

<span data-ttu-id="1d4c2-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="1d4c2-112">S_OK</span></span> 
  
> <span data-ttu-id="1d4c2-113">El identificador de entrada del contenedor predeterminado se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="1d4c2-113">The entry identifier of the default container was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1d4c2-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1d4c2-114">Remarks</span></span>

<span data-ttu-id="1d4c2-115">Proveedores de servicios y aplicaciones cliente de llamar al método **GetDefaultDir** para recuperar el identificador de entrada del contenedor de la libreta de direcciones predeterminada.</span><span class="sxs-lookup"><span data-stu-id="1d4c2-115">Client applications and service providers call the **GetDefaultDir** method to retrieve the entry identifier of the default address book container.</span></span> <span data-ttu-id="1d4c2-116">El contenedor predeterminado es lo que ve el usuario que se muestra en la libreta de direcciones cuando se abre por primera vez la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="1d4c2-116">The default container is what the user sees displayed in the address book when the address book is first opened.</span></span> <span data-ttu-id="1d4c2-117">Si no se ha establecido un contenedor predeterminado mediante una llamada al método [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) , MAPI asigna como el contenedor predeterminado del primer contenedor con nombres que no es la libreta de direcciones personales (PAB).</span><span class="sxs-lookup"><span data-stu-id="1d4c2-117">If a default container has not been set by a call to the [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) method, MAPI assigns as the default container the first container with names that is not the personal address book (PAB).</span></span> <span data-ttu-id="1d4c2-118">Si no se encuentra un contenedor de este tipo, el archivo PAB se convierte en el contenedor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1d4c2-118">If such a container cannot be found, the PAB becomes the default container.</span></span> 
  
<span data-ttu-id="1d4c2-119">Para establecer el valor predeterminado Active directory, un cliente o proveedor llama al método de **SetDefaultDir** .</span><span class="sxs-lookup"><span data-stu-id="1d4c2-119">To set the default directory, a client or provider calls the **SetDefaultDir** method.</span></span> <span data-ttu-id="1d4c2-120">Los clientes y proveedores no es necesario llamar al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) ; debido a que los cambios realizados en la libreta de direcciones no se negocian, cambios se realizan inmediatamente permanentes.</span><span class="sxs-lookup"><span data-stu-id="1d4c2-120">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method; because changes to the address book are not transacted, changes are immediately made permanent.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1d4c2-121">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1d4c2-121">MFCMAPI reference</span></span>

<span data-ttu-id="1d4c2-122">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="1d4c2-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1d4c2-123">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="1d4c2-123">**File**</span></span>|<span data-ttu-id="1d4c2-124">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="1d4c2-124">**Function**</span></span>|<span data-ttu-id="1d4c2-125">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="1d4c2-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1d4c2-126">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="1d4c2-126">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="1d4c2-127">CMainDlg::OnOpenDefaultDir</span><span class="sxs-lookup"><span data-stu-id="1d4c2-127">CMainDlg::OnOpenDefaultDir</span></span>  <br/> |<span data-ttu-id="1d4c2-128">MFCMAPI usa el método **GetDefaultDir** para obtener el identificador para el contenedor de la libreta de direcciones predeterminada.</span><span class="sxs-lookup"><span data-stu-id="1d4c2-128">MFCMAPI uses the **GetDefaultDir** method to get the ID for the default address book container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1d4c2-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d4c2-129">See also</span></span>



[<span data-ttu-id="1d4c2-130">IAddrBook::SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="1d4c2-130">IAddrBook::SetDefaultDir</span></span>](iaddrbook-setdefaultdir.md)
  
[<span data-ttu-id="1d4c2-131">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="1d4c2-131">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="1d4c2-132">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="1d4c2-132">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="1d4c2-133">Propiedad canónica PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="1d4c2-133">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="1d4c2-134">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1d4c2-134">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="1d4c2-135">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="1d4c2-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

