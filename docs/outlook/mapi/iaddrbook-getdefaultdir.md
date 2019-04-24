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
ms.openlocfilehash: d9ad74d8ae02a49ee3c222394caedfd571f84b1c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336697"
---
# <a name="iaddrbookgetdefaultdir"></a><span data-ttu-id="308fb-103">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="308fb-103">IAddrBook::GetDefaultDir</span></span>

  
  
<span data-ttu-id="308fb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="308fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="308fb-105">Devuelve el identificador de entrada del contenedor de libreta de direcciones inicial.</span><span class="sxs-lookup"><span data-stu-id="308fb-105">Returns the entry identifier for the initial address book container.</span></span>
  
```cpp
HRESULT GetDefaultDir(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="308fb-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="308fb-106">Parameters</span></span>

 <span data-ttu-id="308fb-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="308fb-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="308fb-108">contempla Un puntero al recuento de bytes en el identificador de entrada al que apunta el parámetro _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="308fb-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="308fb-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="308fb-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="308fb-110">contempla Un puntero a un puntero al identificador de entrada del contenedor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="308fb-110">[out] A pointer to a pointer to the entry identifier of the default container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="308fb-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="308fb-111">Return value</span></span>

<span data-ttu-id="308fb-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="308fb-112">S_OK</span></span> 
  
> <span data-ttu-id="308fb-113">El identificador de entrada del contenedor predeterminado se ha devuelto correctamente.</span><span class="sxs-lookup"><span data-stu-id="308fb-113">The entry identifier of the default container was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="308fb-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="308fb-114">Remarks</span></span>

<span data-ttu-id="308fb-115">Las aplicaciones cliente y los proveedores de servicios llaman al método **GetDefaultDir** para recuperar el identificador de entrada del contenedor de libreta de direcciones predeterminado.</span><span class="sxs-lookup"><span data-stu-id="308fb-115">Client applications and service providers call the **GetDefaultDir** method to retrieve the entry identifier of the default address book container.</span></span> <span data-ttu-id="308fb-116">El contenedor predeterminado es lo que el usuario ve en la libreta de direcciones cuando se abre por primera vez la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="308fb-116">The default container is what the user sees displayed in the address book when the address book is first opened.</span></span> <span data-ttu-id="308fb-117">Si no se ha establecido un contenedor predeterminado mediante una llamada al método [IAddrBook:: SetDefaultDir](iaddrbook-setdefaultdir.md) , MAPI asignará como el contenedor predeterminado el primer contenedor con nombres que no sea la libreta personal de direcciones (PAB).</span><span class="sxs-lookup"><span data-stu-id="308fb-117">If a default container has not been set by a call to the [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) method, MAPI assigns as the default container the first container with names that is not the personal address book (PAB).</span></span> <span data-ttu-id="308fb-118">Si no se encuentra dicho contenedor, la PAB pasa a ser el contenedor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="308fb-118">If such a container cannot be found, the PAB becomes the default container.</span></span> 
  
<span data-ttu-id="308fb-119">Para establecer el directorio predeterminado, un cliente o proveedor llama al método **SetDefaultDir** .</span><span class="sxs-lookup"><span data-stu-id="308fb-119">To set the default directory, a client or provider calls the **SetDefaultDir** method.</span></span> <span data-ttu-id="308fb-120">Los clientes y proveedores no tienen que llamar al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) ; como los cambios en la libreta de direcciones no se transaccionan, los cambios se realizan inmediatamente de forma permanente.</span><span class="sxs-lookup"><span data-stu-id="308fb-120">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method; because changes to the address book are not transacted, changes are immediately made permanent.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="308fb-121">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="308fb-121">MFCMAPI reference</span></span>

<span data-ttu-id="308fb-122">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="308fb-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="308fb-123">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="308fb-123">**File**</span></span>|<span data-ttu-id="308fb-124">**Función**</span><span class="sxs-lookup"><span data-stu-id="308fb-124">**Function**</span></span>|<span data-ttu-id="308fb-125">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="308fb-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="308fb-126">MainDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="308fb-126">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="308fb-127">CMainDlg:: OnOpenDefaultDir</span><span class="sxs-lookup"><span data-stu-id="308fb-127">CMainDlg::OnOpenDefaultDir</span></span>  <br/> |<span data-ttu-id="308fb-128">MFCMAPI usa el método **GetDefaultDir** para obtener el identificador del contenedor de libreta de direcciones predeterminado.</span><span class="sxs-lookup"><span data-stu-id="308fb-128">MFCMAPI uses the **GetDefaultDir** method to get the ID for the default address book container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="308fb-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="308fb-129">See also</span></span>



[<span data-ttu-id="308fb-130">IAddrBook::SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="308fb-130">IAddrBook::SetDefaultDir</span></span>](iaddrbook-setdefaultdir.md)
  
[<span data-ttu-id="308fb-131">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="308fb-131">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="308fb-132">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="308fb-132">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="308fb-133">Propiedad canónica PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="308fb-133">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="308fb-134">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="308fb-134">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="308fb-135">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="308fb-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

