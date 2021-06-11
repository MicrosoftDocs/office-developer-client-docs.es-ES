---
title: Indicadores de progreso mapi
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
# <a name="mapi-progress-indicators"></a>Indicadores de progreso mapi

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Muchas de las operaciones que realiza para los clientes pueden tardar mucho tiempo en completarse. Para informar a los clientes del progreso de una operación larga, puede mostrar un indicador que muestra gráficamente la parte terminada de una operación en cualquier momento dado desde el inicio de la operación hasta su finalización. El indicador de progreso muestra un porcentaje de la operación total que se va a completar.
  
Los siguientes métodos admiten operaciones largas y la presentación de un indicador de progreso:
  
- [IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::D eleteMessages](imapifolder-deletemessages.md), [IMAPIFolder::D eleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md)y [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md) e [IMAPIProp::CopyTo](imapiprop-copyto.md).
    
- [IMAPISupport::D oCopyProps](imapisupport-docopyprops.md), [IMAPISupport::D oCopyTo](imapisupport-docopyto.md), [IMAPISupport::CopyFolder](imapisupport-copyfolder.md)e [IMAPISupport::CopyMessages](imapisupport-copymessages.md).
    
- [IMessage::D eleteAttach](imessage-deleteattach.md).
    
- [IABContainer::CopyEntries](iabcontainer-copyentries.md).
    
Para mostrar un indicador de progreso, MAPI define un objeto de progreso. Los objetos Progress implementan la interfaz [IMAPIProgress : IUnknown,](imapiprogressiunknown.md) una interfaz que incluye métodos para establecer el intervalo del indicador y crear la pantalla. MAPI proporciona una implementación de objeto de progreso al igual que algunos clientes. Debe usar la implementación de un cliente, si se proporciona uno, como parámetro de entrada para el método que realiza la operación. Si el cliente pasa NULL en lugar de un puntero a un objeto de progreso, use la implementación de MAPI llamando al método [IMAPISupport::D oProgressDialog.](imapisupport-doprogressdialog.md) 
  
## <a name="see-also"></a>Vea también



[Proveedores de servicios MAPI](mapi-service-providers.md)

