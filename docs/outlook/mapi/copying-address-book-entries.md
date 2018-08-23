---
title: Copiar entradas de la libreta de direcciones
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 285abeb4-45c8-4e82-9a16-b935b4651afe
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: eca0c9f63a4efaaa7f9fd066cf5dce451b8f6175
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565889"
---
# <a name="copying-address-book-entries"></a>Copiar entradas de la libreta de direcciones

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Se llama al método de [IABContainer::CopyEntries](iabcontainer-copyentries.md) de su contenedor cuando uno o más destinatarios desde el mismo u otro contenedor que se copiarán a este contenedor. **CopyEntries** tiene cuatro parámetros de entrada: una matriz de identificadores de entrada que representa los destinatarios que se va a copiar, un identificador de ventana para el indicador de progreso, un puntero de objeto de progreso y un valor de indicadores. Su proveedor debe mostrar progreso si la marca AB_NO_DIALOG no está establecida y utilice el objeto de progreso desde el parámetro _lpProgress_ si no es NULL. Si _lpProgress_ es NULL, llame a [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) para usar el objeto de progreso MAPI. Para obtener más información acerca de cómo mostrar progreso, vea [Mostrar un indicador de progreso](mapi-progress-indicators.md).
  
Además de AB_NO_DIALOG para suprimir un indicador de progreso, uno de los otros dos indicadores puede establecerse para solicitar un tipo de comprobación de la entrada duplicada: CREATE_CHECK_DUP_LOOSE o CREATE_CHECK_DUP_STRICT. Los indicadores CREATE_CHECK_DUP_LOOSE y CREATE_CHECK_DUP_STRICT sólo son sugerencias sobre cómo el proveedor determina las entradas duplicadas y se pueden ignorar. MAPI sugiere que su proveedor de implementar la compatibilidad con estos marcadores como se indica a continuación.
  
|**Indicador de entrada duplicada**|**Sugerencia de implementación**|
|:-----|:-----|
|CREATE_CHECK_DUP_LOOSE  <br/> |Comprobar si el nombre para mostrar en la entrada que se creará coincide con el nombre para mostrar de una entrada ya está en el contenedor.  <br/> |
|CREATE_CHECK_DUP_STRICT  <br/> |Compruebe si el nombre para mostrar y la clave de búsqueda en la entrada que se creará coincidir con la clave de búsqueda y de nombre para mostrar de una entrada de contenedor.  <br/> |
   
La última marca, CREATE_REPLACE, indica que la nueva entrada debe reemplazar uno existente si su proveedor ha determinado que una entrada que se va a crear es un duplicado de una entrada ya en su contenedor. 
  
Si su proveedor es una libreta de direcciones personales, incluir la propiedad **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) en cada operación de copia. Incluido en la tabla de detalles para mostrar de un destinatario copiado permite el contenedor mostrar los detalles de destinatario en lugar de tener que llamar el contenedor original para crear la presentación.
  
 **Para implementar IABContainer::CopyEntries**
  
1. Determinar si cada identificador de entrada en el parámetro _lpEntries_ está en un formato que su proveedor controla y si no lo está, producirá un error y devolver MAPI_E_INVALID_ENTRYID. 
    
2. Si un identificador de entrada representa un usuario de mensajería, una lista de distribución o un contenedor que controla su proveedor:
    
1. Llamar al método [IMAPISupport::OpenEntry](imapisupport-openentry.md) para abrir al destinatario correspondiente. 
    
2. Copie al destinatario a su contenedor. 
    
3. Si el identificador de entrada representa a un destinatario externo:
    
1. Llamar al método [IABContainer::CreateEntry](iabcontainer-createentry.md) de su contenedor para crear a un nuevo destinatario. 
    
2. Establecer las propiedades iniciales en el nuevo destinatario.
    
4. Llamar al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) del objeto nuevo para guardarlo. 
    
5. Actualizar la tabla de contenido del contenedor para reflejar al nuevo destinatario. 
    
6. Llame a [IMAPISupport::Notify](imapisupport-notify.md) para enviar una notificación de la tabla a los clientes registrados. 
    

