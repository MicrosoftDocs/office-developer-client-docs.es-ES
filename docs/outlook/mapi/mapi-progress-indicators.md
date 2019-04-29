---
title: Indicadores de progreso de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 73a99e52-97fe-40f5-af90-52cfd858ab22
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: cdfb6898146583b7da9b043eadd3acc09edbf292
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410710"
---
# <a name="mapi-progress-indicators"></a><span data-ttu-id="a0831-103">Indicadores de progreso de MAPI</span><span class="sxs-lookup"><span data-stu-id="a0831-103">MAPI Progress Indicators</span></span>

  
  
<span data-ttu-id="a0831-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0831-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0831-105">Muchas de las operaciones que realiza para los clientes pueden tardar mucho tiempo en completarse.</span><span class="sxs-lookup"><span data-stu-id="a0831-105">Many of the operations that you perform for clients can take a long time to complete.</span></span> <span data-ttu-id="a0831-106">Para informar a los clientes del progreso de una operación prolongada, puede mostrar un indicador que muestre gráficamente la parte terminada de una operación en un punto determinado desde el inicio de la operación hasta su finalización.</span><span class="sxs-lookup"><span data-stu-id="a0831-106">To inform clients of the progress of a lengthy operation, you can show an indicator that displays graphically the finished portion of an operation at any given point from the start of the operation to its completion.</span></span> <span data-ttu-id="a0831-107">El indicador de progreso muestra un porcentaje de la operación total que se va a completar.</span><span class="sxs-lookup"><span data-stu-id="a0831-107">The progress indicator shows a percentage of the total operation to be completed.</span></span>
  
<span data-ttu-id="a0831-108">Los siguientes métodos admiten operaciones de larga duración y la visualización de un indicador de progreso:</span><span class="sxs-lookup"><span data-stu-id="a0831-108">The following methods support lengthy operations and the display of a progress indicator:</span></span>
  
- <span data-ttu-id="a0831-109">[IMAPIFolder:: CopyMessages](imapifolder-copymessages.md), [IMAPIFolder:: CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::D Eletemessages](imapifolder-deletemessages.md), [IMAPIFolder::D Eletefolder](imapifolder-deletefolder.md), [IMAPIFolder:: EmptyFolder](imapifolder-emptyfolder.md)y [IMAPIFolder:: SetReadFlags](imapifolder-setreadflags.md).</span><span class="sxs-lookup"><span data-stu-id="a0831-109">[IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md), [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md), and [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).</span></span>
    
- <span data-ttu-id="a0831-110">[IMAPIProp:: CopyProps](imapiprop-copyprops.md) y [IMAPIProp:: CopyTo](imapiprop-copyto.md).</span><span class="sxs-lookup"><span data-stu-id="a0831-110">[IMAPIProp::CopyProps](imapiprop-copyprops.md) and [IMAPIProp::CopyTo](imapiprop-copyto.md).</span></span>
    
- <span data-ttu-id="a0831-111">[IMAPISupport::D ocopyprops](imapisupport-docopyprops.md), [IMAPISupport::D ocopyto](imapisupport-docopyto.md), [IMAPISupport:: CopyFolder](imapisupport-copyfolder.md)y [IMAPISupport:: CopyMessages](imapisupport-copymessages.md).</span><span class="sxs-lookup"><span data-stu-id="a0831-111">[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md), [IMAPISupport::DoCopyTo](imapisupport-docopyto.md), [IMAPISupport::CopyFolder](imapisupport-copyfolder.md), and [IMAPISupport::CopyMessages](imapisupport-copymessages.md).</span></span>
    
- <span data-ttu-id="a0831-112">[IMessage::D eleteattach](imessage-deleteattach.md).</span><span class="sxs-lookup"><span data-stu-id="a0831-112">[IMessage::DeleteAttach](imessage-deleteattach.md).</span></span>
    
- <span data-ttu-id="a0831-113">[IABContainer:: CopyEntries](iabcontainer-copyentries.md).</span><span class="sxs-lookup"><span data-stu-id="a0831-113">[IABContainer::CopyEntries](iabcontainer-copyentries.md).</span></span>
    
<span data-ttu-id="a0831-114">Para mostrar un indicador de progreso, MAPI define un objeto de progreso.</span><span class="sxs-lookup"><span data-stu-id="a0831-114">To display a progress indicator, MAPI defines a progress object.</span></span> <span data-ttu-id="a0831-115">Los objetos de progreso implementan la interfaz [método imapiprogress: IUnknown](imapiprogressiunknown.md) , una interfaz que incluye métodos para establecer el intervalo del indicador y crear la presentación.</span><span class="sxs-lookup"><span data-stu-id="a0831-115">Progress objects implement the [IMAPIProgress : IUnknown](imapiprogressiunknown.md) interface, an interface that includes methods for establishing the range of the indicator and creating the display.</span></span> <span data-ttu-id="a0831-116">MAPI proporciona una implementación de objetos de progreso como algunos clientes.</span><span class="sxs-lookup"><span data-stu-id="a0831-116">MAPI provides a progress object implementation as do some clients.</span></span> <span data-ttu-id="a0831-117">Debe usar la implementación de un cliente, si se proporciona una, como parámetro de entrada para el método que realiza la operación.</span><span class="sxs-lookup"><span data-stu-id="a0831-117">You should use a client's implementation, if one is supplied, as an input parameter to the method performing the operation.</span></span> <span data-ttu-id="a0831-118">Si el cliente pasa NULL en lugar de un puntero a un objeto Progress, use la implementación de MAPI llamando al método [IMAPISupport::D oprogressdialog](imapisupport-doprogressdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="a0831-118">If the client passes NULL instead of a pointer to a progress object, use MAPI's implementation by calling the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a0831-119">Ver también</span><span class="sxs-lookup"><span data-stu-id="a0831-119">See also</span></span>



[<span data-ttu-id="a0831-120">Proveedores de servicios MAPI</span><span class="sxs-lookup"><span data-stu-id="a0831-120">MAPI Service Providers</span></span>](mapi-service-providers.md)

