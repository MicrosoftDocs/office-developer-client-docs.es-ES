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
ms.openlocfilehash: 8539f81ed1741063d878da492d925b63c488d1a9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586434"
---
# <a name="iproxystoreobjectunwrapnoref"></a><span data-ttu-id="4f602-103">IProxyStoreObject::UnwrapNoRef</span><span class="sxs-lookup"><span data-stu-id="4f602-103">IProxyStoreObject::UnwrapNoRef</span></span>

  
  
<span data-ttu-id="4f602-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f602-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f602-105">Obtiene un puntero a un objeto de almacén de protocolo de acceso a mensajes de Internet (IMAP) no ajustado que proporciona acceso al archivo de carpetas personales (PST) subyacente sin invocar la sincronización y descarga de los elementos.</span><span class="sxs-lookup"><span data-stu-id="4f602-105">Gets a pointer to an unwrapped Internet Message Access Protocol (IMAP) store object that provides access to the underlying Personal Folders file (PST) without invoking synchronization and downloading the items.</span></span>
  
```cpp
HRESULT IProxyStoreObject::UnwrapNoRef (     LPVOID *ppvObject ); 
```

## <a name="parameters"></a><span data-ttu-id="4f602-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4f602-106">Parameters</span></span>

 <span data-ttu-id="4f602-107">_ppvObject_</span><span class="sxs-lookup"><span data-stu-id="4f602-107">_ppvObject_</span></span>
  
> <span data-ttu-id="4f602-108">[out] Puntero a un [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) objeto store que se no ajustado.</span><span class="sxs-lookup"><span data-stu-id="4f602-108">[out] Pointer to an [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) store object that is unwrapped.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="4f602-109">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="4f602-109">Return values</span></span>

<span data-ttu-id="4f602-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="4f602-110">S_OK</span></span>
  
- <span data-ttu-id="4f602-111">La llamada se realizó correctamente y se ha devuelto un puntero a una interfaz no ajustado en _ppvObject_.</span><span class="sxs-lookup"><span data-stu-id="4f602-111">The call was successful and a pointer to an unwrapped interface has been returned in  _ppvObject_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4f602-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4f602-112">Remarks</span></span>

<span data-ttu-id="4f602-113">Sin primera apertura un almacén IMAP, obtener acceso a un mensaje en el almacén puede forzar la sincronización que intenta descargar el mensaje completo.</span><span class="sxs-lookup"><span data-stu-id="4f602-113">Without first unwrapping an IMAP store, accessing a message in the store can force a synchronization that attempts to download the entire message.</span></span> <span data-ttu-id="4f602-114">Mediante el almacén no ajustado permite el acceso a los mensajes en su estado actual sin desencadenar una descarga.</span><span class="sxs-lookup"><span data-stu-id="4f602-114">Using the unwrapped store allows access to the message in its current state without triggering a download.</span></span>
  
<span data-ttu-id="4f602-115">Debido a que **UnwrapNoRef** no incrementa el recuento de referencias para este nuevo puntero al objeto de almacén no ajustado, después de llamar correctamente a **UnwrapNoRef**, se debe llamar a [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) para mantener el recuento de referencia.</span><span class="sxs-lookup"><span data-stu-id="4f602-115">Because **UnwrapNoRef** does not increment the reference count for this new pointer to the unwrapped store object, after successfully calling **UnwrapNoRef**, you should call [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) to maintain the reference count.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4f602-116">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="4f602-116">See also</span></span>



[<span data-ttu-id="4f602-117">IProxyStoreObject</span><span class="sxs-lookup"><span data-stu-id="4f602-117">IProxyStoreObject</span></span>](iproxystoreobject.md)

