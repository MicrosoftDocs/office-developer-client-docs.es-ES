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
ms.openlocfilehash: 1f93ee653c9365488432c4e797b171a199c30107
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583718"
---
# <a name="iaddrbookgetpab"></a><span data-ttu-id="3b5f2-103">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="3b5f2-103">IAddrBook::GetPAB</span></span>

  
  
<span data-ttu-id="3b5f2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b5f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b5f2-105">Devuelve el identificador de entrada del contenedor que se designa como la libreta de direcciones personales (PAB).</span><span class="sxs-lookup"><span data-stu-id="3b5f2-105">Returns the entry identifier of the container that is designated as the personal address book (PAB).</span></span>
  
```cpp
HRESULT GetPAB(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="3b5f2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b5f2-106">Parameters</span></span>

 <span data-ttu-id="3b5f2-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="3b5f2-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="3b5f2-108">[out] Un puntero para el número de bytes en el identificador de entrada indicado por el parámetro _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="3b5f2-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="3b5f2-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="3b5f2-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="3b5f2-110">[out] Un puntero a un puntero al identificador de entrada de la Libreta personal de direcciones.</span><span class="sxs-lookup"><span data-stu-id="3b5f2-110">[out] A pointer to a pointer to the entry identifier of the PAB.</span></span> <span data-ttu-id="3b5f2-111">El parámetro _lppEntryID_ contiene cero si no se ha designado ningún contenedor como el archivo PAB.</span><span class="sxs-lookup"><span data-stu-id="3b5f2-111">The  _lppEntryID_ parameter contains zero if no container has been designated as the PAB.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3b5f2-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b5f2-112">Return value</span></span>

<span data-ttu-id="3b5f2-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="3b5f2-113">S_OK</span></span> 
  
> <span data-ttu-id="3b5f2-114">El identificador de entrada de la Libreta personal de direcciones se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="3b5f2-114">The entry identifier of the PAB was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3b5f2-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3b5f2-115">Remarks</span></span>

<span data-ttu-id="3b5f2-116">Los clientes de llaman al método **GetPAB** para recuperar el identificador de entrada del contenedor designado como el archivo PAB.</span><span class="sxs-lookup"><span data-stu-id="3b5f2-116">Clients call the **GetPAB** method to retrieve the entry identifier of the container designated as the PAB.</span></span> <span data-ttu-id="3b5f2-117">Si no se ha establecido una libreta personal de direcciones en el perfil, MAPI selecciona como el archivo PAB del primer contenedor en la jerarquía de la libreta de direcciones que permite que las modificaciones.</span><span class="sxs-lookup"><span data-stu-id="3b5f2-117">If a PAB has not been established in the profile, MAPI selects as the PAB the first container in the address book hierarchy that allows modifications.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3b5f2-118">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3b5f2-118">MFCMAPI reference</span></span>

<span data-ttu-id="3b5f2-119">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="3b5f2-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3b5f2-120">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="3b5f2-120">**File**</span></span>|<span data-ttu-id="3b5f2-121">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="3b5f2-121">**Function**</span></span>|<span data-ttu-id="3b5f2-122">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="3b5f2-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3b5f2-123">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="3b5f2-123">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="3b5f2-124">CMainDlg::OnOpenPAB</span><span class="sxs-lookup"><span data-stu-id="3b5f2-124">CMainDlg::OnOpenPAB</span></span>  <br/> |<span data-ttu-id="3b5f2-125">MFCMAPI usa el método **GetPAB** para obtener el identificador de la libreta de direcciones personales del usuario.</span><span class="sxs-lookup"><span data-stu-id="3b5f2-125">MFCMAPI uses the **GetPAB** method to get the ID for the user's personal address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3b5f2-126">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="3b5f2-126">See also</span></span>



[<span data-ttu-id="3b5f2-127">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="3b5f2-127">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="3b5f2-128">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="3b5f2-128">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="3b5f2-129">Propiedad canónica PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="3b5f2-129">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="3b5f2-130">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3b5f2-130">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="3b5f2-131">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="3b5f2-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

