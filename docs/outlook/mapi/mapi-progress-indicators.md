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
ms.openlocfilehash: 8fc39c6d7da0970ee15cdd9dd67bfeef0997d7d1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582871"
---
# <a name="mapi-progress-indicators"></a>Indicadores de progreso MAPI

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Muchas de las operaciones que se realizan para los clientes pueden tardar mucho tiempo en completarse. Para informar a los clientes del progreso de una operación prolongada, puede mostrar un indicador que muestra gráficamente la termine de parte de una operación en cualquier momento determinado desde el comienzo de la operación hasta su finalización. El indicador de progreso muestra un porcentaje de la operación de total.
  
Los siguientes métodos admiten operaciones largas y la visualización de un indicador de progreso:
  
- [IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md), [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md)y [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md) y [IMAPIProp::CopyTo](imapiprop-copyto.md).
    
- [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md), [IMAPISupport::DoCopyTo](imapisupport-docopyto.md), [IMAPISupport::CopyFolder](imapisupport-copyfolder.md)y [IMAPISupport::CopyMessages](imapisupport-copymessages.md).
    
- [IMessage::DeleteAttach](imessage-deleteattach.md).
    
- [IABContainer::CopyEntries](iabcontainer-copyentries.md).
    
Para mostrar un indicador de progreso, MAPI define un objeto de progreso. Objetos de progreso implementan el [IMAPIProgress: IUnknown](imapiprogressiunknown.md) interfaz, una interfaz que incluye métodos para establecer el intervalo del indicador y crear la presentación. MAPI proporciona una implementación de objeto de progreso como hacer algunos clientes. Debe usar la implementación de un cliente, si se proporciona una, como un parámetro de entrada para el método a realizar la operación. Si el cliente pasa NULL en lugar de un puntero a un objeto de progreso, utilice la implementación de MAPI llamando al método [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) . 
  
## <a name="see-also"></a>Vea también



[Proveedores de servicios de MAPI](mapi-service-providers.md)

