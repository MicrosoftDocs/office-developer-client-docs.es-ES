---
title: Indicadores de progreso MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 73a99e52-97fe-40f5-af90-52cfd858ab22
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d8af2ba3067dabe759056313eb278b9901510980
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818174"
---
# <a name="mapi-progress-indicators"></a><span data-ttu-id="d9b84-103">Indicadores de progreso MAPI</span><span class="sxs-lookup"><span data-stu-id="d9b84-103">MAPI Progress Indicators</span></span>

  
  
<span data-ttu-id="d9b84-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d9b84-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d9b84-105">Muchas de las operaciones que se realizan para los clientes pueden tardar mucho tiempo en completarse.</span><span class="sxs-lookup"><span data-stu-id="d9b84-105">Many of the operations that you perform for clients can take a long time to complete.</span></span> <span data-ttu-id="d9b84-106">Para informar a los clientes del progreso de una operación prolongada, puede mostrar un indicador que muestra gráficamente la termine de parte de una operación en cualquier momento determinado desde el comienzo de la operación hasta su finalización.</span><span class="sxs-lookup"><span data-stu-id="d9b84-106">To inform clients of the progress of a lengthy operation, you can show an indicator that displays graphically the finished portion of an operation at any given point from the start of the operation to its completion.</span></span> <span data-ttu-id="d9b84-107">El indicador de progreso muestra un porcentaje de la operación de total.</span><span class="sxs-lookup"><span data-stu-id="d9b84-107">The progress indicator shows a percentage of the total operation to be completed.</span></span>
  
<span data-ttu-id="d9b84-108">Los siguientes métodos admiten operaciones largas y la visualización de un indicador de progreso:</span><span class="sxs-lookup"><span data-stu-id="d9b84-108">The following methods support lengthy operations and the display of a progress indicator:</span></span>
  
- <span data-ttu-id="d9b84-109">[IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md), [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md)y [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).</span><span class="sxs-lookup"><span data-stu-id="d9b84-109">[IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md), [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md), and [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).</span></span>
    
- <span data-ttu-id="d9b84-110">[IMAPIProp::CopyProps](imapiprop-copyprops.md) y [IMAPIProp::CopyTo](imapiprop-copyto.md).</span><span class="sxs-lookup"><span data-stu-id="d9b84-110">[IMAPIProp::CopyProps](imapiprop-copyprops.md) and [IMAPIProp::CopyTo](imapiprop-copyto.md).</span></span>
    
- <span data-ttu-id="d9b84-111">[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md), [IMAPISupport::DoCopyTo](imapisupport-docopyto.md), [IMAPISupport::CopyFolder](imapisupport-copyfolder.md)y [IMAPISupport::CopyMessages](imapisupport-copymessages.md).</span><span class="sxs-lookup"><span data-stu-id="d9b84-111">[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md), [IMAPISupport::DoCopyTo](imapisupport-docopyto.md), [IMAPISupport::CopyFolder](imapisupport-copyfolder.md), and [IMAPISupport::CopyMessages](imapisupport-copymessages.md).</span></span>
    
- <span data-ttu-id="d9b84-112">[IMessage::DeleteAttach](imessage-deleteattach.md).</span><span class="sxs-lookup"><span data-stu-id="d9b84-112">[IMessage::DeleteAttach](imessage-deleteattach.md).</span></span>
    
- <span data-ttu-id="d9b84-113">[IABContainer::CopyEntries](iabcontainer-copyentries.md).</span><span class="sxs-lookup"><span data-stu-id="d9b84-113">[IABContainer::CopyEntries](iabcontainer-copyentries.md).</span></span>
    
<span data-ttu-id="d9b84-114">Para mostrar un indicador de progreso, MAPI define un objeto de progreso.</span><span class="sxs-lookup"><span data-stu-id="d9b84-114">To display a progress indicator, MAPI defines a progress object.</span></span> <span data-ttu-id="d9b84-115">Objetos de progreso implementan el [IMAPIProgress: IUnknown](imapiprogressiunknown.md) interfaz, una interfaz que incluye métodos para establecer el intervalo del indicador y crear la presentación.</span><span class="sxs-lookup"><span data-stu-id="d9b84-115">Progress objects implement the [IMAPIProgress : IUnknown](imapiprogressiunknown.md) interface, an interface that includes methods for establishing the range of the indicator and creating the display.</span></span> <span data-ttu-id="d9b84-116">MAPI proporciona una implementación de objeto de progreso como hacer algunos clientes.</span><span class="sxs-lookup"><span data-stu-id="d9b84-116">MAPI provides a progress object implementation as do some clients.</span></span> <span data-ttu-id="d9b84-117">Debe usar la implementación de un cliente, si se proporciona una, como un parámetro de entrada para el método a realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="d9b84-117">You should use a client's implementation, if one is supplied, as an input parameter to the method performing the operation.</span></span> <span data-ttu-id="d9b84-118">Si el cliente pasa NULL en lugar de un puntero a un objeto de progreso, utilice la implementación de MAPI llamando al método [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="d9b84-118">If the client passes NULL instead of a pointer to a progress object, use MAPI's implementation by calling the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d9b84-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9b84-119">See also</span></span>



[<span data-ttu-id="d9b84-120">Proveedores de servicios de MAPI</span><span class="sxs-lookup"><span data-stu-id="d9b84-120">MAPI Service Providers</span></span>](mapi-service-providers.md)
