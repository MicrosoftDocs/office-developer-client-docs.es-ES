---
title: IProxyStoreObject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProxyStoreObject
api_type:
- COM
ms.assetid: 567bede4-39a3-bfb4-af85-ba678e2cf4a5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b842bee8d9e243aa38bafe39d786a31b5527b054
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567947"
---
# <a name="iproxystoreobject"></a><span data-ttu-id="1fa37-103">IProxyStoreObject</span><span class="sxs-lookup"><span data-stu-id="1fa37-103">IProxyStoreObject</span></span>

  
  
<span data-ttu-id="1fa37-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1fa37-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1fa37-105">Proporciona un objeto de almacén de protocolo de acceso a mensajes de Internet (IMAP) que ha sido no ajustado y que permite el acceso a los elementos en el archivo de carpetas personales (PST) sin invocar la sincronización y descarga de los elementos.</span><span class="sxs-lookup"><span data-stu-id="1fa37-105">Provides an Internet Message Access Protocol (IMAP) store object that has been unwrapped and that allows access to items in the Personal Folders file (PST) without invoking synchronization and downloading the items.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1fa37-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="1fa37-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1fa37-107">Heredado de:</span><span class="sxs-lookup"><span data-stu-id="1fa37-107">Inherited from:</span></span>  <br/> |[<span data-ttu-id="1fa37-108">IUnknown</span><span class="sxs-lookup"><span data-stu-id="1fa37-108">IUnknown</span></span>](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) <br/> |
|<span data-ttu-id="1fa37-109">Proporcionado por:</span><span class="sxs-lookup"><span data-stu-id="1fa37-109">Provided By:</span></span>  <br/> |<span data-ttu-id="1fa37-110">Proveedor de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="1fa37-110">Message store provider</span></span>  <br/> |
|<span data-ttu-id="1fa37-111">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="1fa37-111">Interface identifier:</span></span>  <br/> |<span data-ttu-id="1fa37-112">**IID_IProxyStoreObject**</span><span class="sxs-lookup"><span data-stu-id="1fa37-112">**IID_IProxyStoreObject**</span></span> <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="1fa37-113">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="1fa37-113">Vtable order</span></span>

|||
|:-----|:-----|
| <span data-ttu-id="1fa37-114">*Miembro de marcador de posición*</span><span class="sxs-lookup"><span data-stu-id="1fa37-114">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="1fa37-115">*No se admiten o documentado.*</span><span class="sxs-lookup"><span data-stu-id="1fa37-115">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="1fa37-116">IProxyStoreObject::UnwrapNoRef</span><span class="sxs-lookup"><span data-stu-id="1fa37-116">IProxyStoreObject::UnwrapNoRef</span></span>](iproxystoreobject-unwrapnoref.md) <br/> |<span data-ttu-id="1fa37-117">Obtiene un puntero a un almacén IMAP no ajustado.</span><span class="sxs-lookup"><span data-stu-id="1fa37-117">Gets a pointer to an unwrapped IMAP store.</span></span>  <br/> |
| <span data-ttu-id="1fa37-118">*Miembro de marcador de posición*</span><span class="sxs-lookup"><span data-stu-id="1fa37-118">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="1fa37-119">*No se admiten o documentado.*</span><span class="sxs-lookup"><span data-stu-id="1fa37-119">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1fa37-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1fa37-120">Remarks</span></span>

<span data-ttu-id="1fa37-121">Llamar a [IUnknown:: QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) en el almacén de mensajes de origen para obtener la interfaz **IProxyStoreObject** .</span><span class="sxs-lookup"><span data-stu-id="1fa37-121">Call [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) on the source message store to obtain the **IProxyStoreObject** interface.</span></span> <span data-ttu-id="1fa37-122">A continuación, llame a **IProxyStoreObject::UnwrapNoRef** para obtener el objeto de almacén no ajustado.</span><span class="sxs-lookup"><span data-stu-id="1fa37-122">Then call **IProxyStoreObject::UnwrapNoRef** to obtain the unwrapped store object.</span></span> <span data-ttu-id="1fa37-123">Si **QueryInterface** devuelve el error **MAPI_E_INTERFACE_NOT_SUPPORTED**, el almacén no se ha ajustado.</span><span class="sxs-lookup"><span data-stu-id="1fa37-123">If **QueryInterface** returns the error **MAPI_E_INTERFACE_NOT_SUPPORTED**, then the store has not been wrapped.</span></span> 
  
<span data-ttu-id="1fa37-124">Debido a que **UnwrapNoRef** no incrementa el recuento de referencias para este nuevo puntero al objeto de almacén no ajustado, después de llamar correctamente a **UnwrapNoRef**, se debe llamar a [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) para mantener el recuento de referencia.</span><span class="sxs-lookup"><span data-stu-id="1fa37-124">Because **UnwrapNoRef** does not increment the reference count for this new pointer to the unwrapped store object, after successfully calling **UnwrapNoRef**, you should call [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) to maintain the reference count.</span></span> 
  

