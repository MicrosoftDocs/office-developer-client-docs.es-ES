---
title: IAddrBookGetPAB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetPAB
api_type:
- COM
ms.assetid: 9830e09c-700f-469b-a54d-4e4e0583aa84
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6c565c088fd4ef7d5df141bf770c560f79535998
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419901"
---
# <a name="iaddrbookgetpab"></a><span data-ttu-id="e49b3-103">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="e49b3-103">IAddrBook::GetPAB</span></span>

  
  
<span data-ttu-id="e49b3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e49b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e49b3-105">Devuelve el identificador de entrada del contenedor que se ha designado como la libreta personal de direcciones (PAB).</span><span class="sxs-lookup"><span data-stu-id="e49b3-105">Returns the entry identifier of the container that is designated as the personal address book (PAB).</span></span>
  
```cpp
HRESULT GetPAB(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="e49b3-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="e49b3-106">Parameters</span></span>

 <span data-ttu-id="e49b3-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="e49b3-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="e49b3-108">contempla Un puntero al recuento de bytes en el identificador de entrada al que apunta el parámetro _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="e49b3-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="e49b3-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="e49b3-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="e49b3-110">contempla Un puntero a un puntero al identificador de entrada de la PAB.</span><span class="sxs-lookup"><span data-stu-id="e49b3-110">[out] A pointer to a pointer to the entry identifier of the PAB.</span></span> <span data-ttu-id="e49b3-111">El parámetro _lppEntryID_ contiene cero si no hay ningún contenedor designado como PAB.</span><span class="sxs-lookup"><span data-stu-id="e49b3-111">The  _lppEntryID_ parameter contains zero if no container has been designated as the PAB.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e49b3-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e49b3-112">Return value</span></span>

<span data-ttu-id="e49b3-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="e49b3-113">S_OK</span></span> 
  
> <span data-ttu-id="e49b3-114">El identificador de entrada de la PAB se ha devuelto correctamente.</span><span class="sxs-lookup"><span data-stu-id="e49b3-114">The entry identifier of the PAB was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e49b3-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e49b3-115">Remarks</span></span>

<span data-ttu-id="e49b3-116">Los clientes llaman al método **GetPAB** para recuperar el identificador de entrada del contenedor designado como PAB.</span><span class="sxs-lookup"><span data-stu-id="e49b3-116">Clients call the **GetPAB** method to retrieve the entry identifier of the container designated as the PAB.</span></span> <span data-ttu-id="e49b3-117">Si no se ha establecido una PAB en el perfil, MAPI selecciona como PAB el primer contenedor de la jerarquía de libretas de direcciones que permite realizar modificaciones.</span><span class="sxs-lookup"><span data-stu-id="e49b3-117">If a PAB has not been established in the profile, MAPI selects as the PAB the first container in the address book hierarchy that allows modifications.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e49b3-118">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e49b3-118">MFCMAPI reference</span></span>

<span data-ttu-id="e49b3-119">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="e49b3-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e49b3-120">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="e49b3-120">**File**</span></span>|<span data-ttu-id="e49b3-121">**Función**</span><span class="sxs-lookup"><span data-stu-id="e49b3-121">**Function**</span></span>|<span data-ttu-id="e49b3-122">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="e49b3-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e49b3-123">MainDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="e49b3-123">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="e49b3-124">CMainDlg:: OnOpenPAB</span><span class="sxs-lookup"><span data-stu-id="e49b3-124">CMainDlg::OnOpenPAB</span></span>  <br/> |<span data-ttu-id="e49b3-125">MFCMAPI usa el método **GetPAB** para obtener el identificador de la libreta personal de direcciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="e49b3-125">MFCMAPI uses the **GetPAB** method to get the ID for the user's personal address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e49b3-126">Ver también</span><span class="sxs-lookup"><span data-stu-id="e49b3-126">See also</span></span>



[<span data-ttu-id="e49b3-127">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="e49b3-127">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="e49b3-128">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="e49b3-128">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="e49b3-129">Propiedad canónica PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="e49b3-129">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="e49b3-130">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e49b3-130">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="e49b3-131">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="e49b3-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

