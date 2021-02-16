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
ms.openlocfilehash: 485d3f3cd4b6be4748a2ebf2ba0d0b71f691478f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315522"
---
# <a name="iproxystoreobject"></a><span data-ttu-id="62cdb-103">IProxyStoreObject</span><span class="sxs-lookup"><span data-stu-id="62cdb-103">IProxyStoreObject</span></span>

  
  
<span data-ttu-id="62cdb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62cdb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62cdb-105">Proporciona un objeto de almacén del Protocolo de acceso a mensajes de Internet (IMAP) que se ha desencapsulado y que permite el acceso a los elementos del archivo de carpetas personales (PST) sin invocar la sincronización y descargar los elementos.</span><span class="sxs-lookup"><span data-stu-id="62cdb-105">Provides an Internet Message Access Protocol (IMAP) store object that has been unwrapped and that allows access to items in the Personal Folders file (PST) without invoking synchronization and downloading the items.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="62cdb-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="62cdb-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="62cdb-107">Heredado de:</span><span class="sxs-lookup"><span data-stu-id="62cdb-107">Inherited from:</span></span>  <br/> |[<span data-ttu-id="62cdb-108">IUnknown</span><span class="sxs-lookup"><span data-stu-id="62cdb-108">IUnknown</span></span>](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) <br/> |
|<span data-ttu-id="62cdb-109">Proporcionado por:</span><span class="sxs-lookup"><span data-stu-id="62cdb-109">Provided By:</span></span>  <br/> |<span data-ttu-id="62cdb-110">Proveedor de almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="62cdb-110">Message store provider</span></span>  <br/> |
|<span data-ttu-id="62cdb-111">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="62cdb-111">Interface identifier:</span></span>  <br/> |<span data-ttu-id="62cdb-112">**IID_IProxyStoreObject**</span><span class="sxs-lookup"><span data-stu-id="62cdb-112">**IID_IProxyStoreObject**</span></span> <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="62cdb-113">Orden de tabla virtual</span><span class="sxs-lookup"><span data-stu-id="62cdb-113">Vtable order</span></span>

|||
|:-----|:-----|
| <span data-ttu-id="62cdb-114">*Miembro de marcador de posición*</span><span class="sxs-lookup"><span data-stu-id="62cdb-114">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="62cdb-115">*No se admite ni se documenta.*</span><span class="sxs-lookup"><span data-stu-id="62cdb-115">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="62cdb-116">IProxyStoreObject::UnwrapNoRef</span><span class="sxs-lookup"><span data-stu-id="62cdb-116">IProxyStoreObject::UnwrapNoRef</span></span>](iproxystoreobject-unwrapnoref.md) <br/> |<span data-ttu-id="62cdb-117">Obtiene un puntero a un almacén IMAP sin envolver.</span><span class="sxs-lookup"><span data-stu-id="62cdb-117">Gets a pointer to an unwrapped IMAP store.</span></span>  <br/> |
| <span data-ttu-id="62cdb-118">*Miembro de marcador de posición*</span><span class="sxs-lookup"><span data-stu-id="62cdb-118">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="62cdb-119">*No se admite ni se documenta.*</span><span class="sxs-lookup"><span data-stu-id="62cdb-119">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="62cdb-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="62cdb-120">Remarks</span></span>

<span data-ttu-id="62cdb-121">Llame [a IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) en el almacén de mensajes de origen para obtener la **interfaz IProxyStoreObject.**</span><span class="sxs-lookup"><span data-stu-id="62cdb-121">Call [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) on the source message store to obtain the **IProxyStoreObject** interface.</span></span> <span data-ttu-id="62cdb-122">A **continuación, llama a IProxyStoreObject::UnwrapNoRef para** obtener el objeto de almacén sin envolver.</span><span class="sxs-lookup"><span data-stu-id="62cdb-122">Then call **IProxyStoreObject::UnwrapNoRef** to obtain the unwrapped store object.</span></span> <span data-ttu-id="62cdb-123">Si **QueryInterface** devuelve el error **MAPI_E_INTERFACE_NOT_SUPPORTED**, el almacén no se ha ajustado.</span><span class="sxs-lookup"><span data-stu-id="62cdb-123">If **QueryInterface** returns the error **MAPI_E_INTERFACE_NOT_SUPPORTED**, then the store has not been wrapped.</span></span> 
  
<span data-ttu-id="62cdb-124">Dado que **UnwrapNoRef** no incrementa el recuento de referencias para este nuevo puntero al objeto de almacén sin envolver, después de llamar correctamente **a UnwrapNoRef**, debe llamar a [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) para mantener el recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="62cdb-124">Because **UnwrapNoRef** does not increment the reference count for this new pointer to the unwrapped store object, after successfully calling **UnwrapNoRef**, you should call [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) to maintain the reference count.</span></span> 
  

