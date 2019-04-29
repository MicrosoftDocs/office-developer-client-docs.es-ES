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
# <a name="mapi-progress-indicators"></a>Indicadores de progreso de MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Muchas de las operaciones que realiza para los clientes pueden tardar mucho tiempo en completarse. Para informar a los clientes del progreso de una operación prolongada, puede mostrar un indicador que muestre gráficamente la parte terminada de una operación en un punto determinado desde el inicio de la operación hasta su finalización. El indicador de progreso muestra un porcentaje de la operación total que se va a completar.
  
Los siguientes métodos admiten operaciones de larga duración y la visualización de un indicador de progreso:
  
- [IMAPIFolder:: CopyMessages](imapifolder-copymessages.md), [IMAPIFolder:: CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::D Eletemessages](imapifolder-deletemessages.md), [IMAPIFolder::D Eletefolder](imapifolder-deletefolder.md), [IMAPIFolder:: EmptyFolder](imapifolder-emptyfolder.md)y [IMAPIFolder:: SetReadFlags](imapifolder-setreadflags.md).
    
- [IMAPIProp:: CopyProps](imapiprop-copyprops.md) y [IMAPIProp:: CopyTo](imapiprop-copyto.md).
    
- [IMAPISupport::D ocopyprops](imapisupport-docopyprops.md), [IMAPISupport::D ocopyto](imapisupport-docopyto.md), [IMAPISupport:: CopyFolder](imapisupport-copyfolder.md)y [IMAPISupport:: CopyMessages](imapisupport-copymessages.md).
    
- [IMessage::D eleteattach](imessage-deleteattach.md).
    
- [IABContainer:: CopyEntries](iabcontainer-copyentries.md).
    
Para mostrar un indicador de progreso, MAPI define un objeto de progreso. Los objetos de progreso implementan la interfaz [método imapiprogress: IUnknown](imapiprogressiunknown.md) , una interfaz que incluye métodos para establecer el intervalo del indicador y crear la presentación. MAPI proporciona una implementación de objetos de progreso como algunos clientes. Debe usar la implementación de un cliente, si se proporciona una, como parámetro de entrada para el método que realiza la operación. Si el cliente pasa NULL en lugar de un puntero a un objeto Progress, use la implementación de MAPI llamando al método [IMAPISupport::D oprogressdialog](imapisupport-doprogressdialog.md) . 
  
## <a name="see-also"></a>Ver también



[Proveedores de servicios MAPI](mapi-service-providers.md)

