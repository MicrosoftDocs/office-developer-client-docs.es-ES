---
title: IProxyStoreObjectUnwrapNoRef
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProxyStoreObject.UnwrapNoRef
api_type:
- COM
ms.assetid: 1122b6e0-e7e1-e68a-e090-435777343d04
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ef9f506c1a95fec86c7f092b0299198e6149d3ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320156"
---
# <a name="iproxystoreobjectunwrapnoref"></a><span data-ttu-id="a487b-103">IProxyStoreObject::UnwrapNoRef</span><span class="sxs-lookup"><span data-stu-id="a487b-103">IProxyStoreObject::UnwrapNoRef</span></span>

  
  
<span data-ttu-id="a487b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a487b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a487b-105">Obtiene un puntero a un objeto de almacén IMAP (Protocolo de acceso a mensajes de Internet) sin ajustar que proporciona acceso al archivo de carpetas personales (PST) subyacente sin invocar la sincronización y descargar los elementos.</span><span class="sxs-lookup"><span data-stu-id="a487b-105">Gets a pointer to an unwrapped Internet Message Access Protocol (IMAP) store object that provides access to the underlying Personal Folders file (PST) without invoking synchronization and downloading the items.</span></span>
  
```cpp
HRESULT IProxyStoreObject::UnwrapNoRef (     LPVOID *ppvObject ); 
```

## <a name="parameters"></a><span data-ttu-id="a487b-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="a487b-106">Parameters</span></span>

 <span data-ttu-id="a487b-107">_ppvObject_</span><span class="sxs-lookup"><span data-stu-id="a487b-107">_ppvObject_</span></span>
  
> <span data-ttu-id="a487b-108">contempla Puntero a un objeto Store de [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) que se desenvuelve.</span><span class="sxs-lookup"><span data-stu-id="a487b-108">[out] Pointer to an [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) store object that is unwrapped.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="a487b-109">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="a487b-109">Return values</span></span>

<span data-ttu-id="a487b-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="a487b-110">S_OK</span></span>
  
- <span data-ttu-id="a487b-111">La llamada se ha realizado correctamente y se ha devuelto un puntero a una interfaz desempaquetada en _ppvObject_.</span><span class="sxs-lookup"><span data-stu-id="a487b-111">The call was successful and a pointer to an unwrapped interface has been returned in  _ppvObject_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a487b-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a487b-112">Remarks</span></span>

<span data-ttu-id="a487b-113">Si no se desenvuelve primero un almacén IMAP, el acceso a un mensaje en la tienda puede forzar una sincronización que intente descargar el mensaje completo.</span><span class="sxs-lookup"><span data-stu-id="a487b-113">Without first unwrapping an IMAP store, accessing a message in the store can force a synchronization that attempts to download the entire message.</span></span> <span data-ttu-id="a487b-114">El uso del almacén desempaquetado permite el acceso al mensaje en su estado actual sin desencadenar una descarga.</span><span class="sxs-lookup"><span data-stu-id="a487b-114">Using the unwrapped store allows access to the message in its current state without triggering a download.</span></span>
  
<span data-ttu-id="a487b-115">Dado que **UnwrapNoRef** no incrementa el recuento de referencias para este nuevo puntero al objeto de almacén desencapsulado, después de llamar a **UnwrapNoRef**correctamente, debe llamar a [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) para mantener el recuento de referencia.</span><span class="sxs-lookup"><span data-stu-id="a487b-115">Because **UnwrapNoRef** does not increment the reference count for this new pointer to the unwrapped store object, after successfully calling **UnwrapNoRef**, you should call [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) to maintain the reference count.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a487b-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="a487b-116">See also</span></span>



[<span data-ttu-id="a487b-117">IProxyStoreObject</span><span class="sxs-lookup"><span data-stu-id="a487b-117">IProxyStoreObject</span></span>](iproxystoreobject.md)

