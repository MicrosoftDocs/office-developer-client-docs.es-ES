---
title: Copiar entradas de libreta de direcciones
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 285abeb4-45c8-4e82-9a16-b935b4651afe
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 190c4bf12c8f5aaaf8143f59239bb53fb68046f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418746"
---
# <a name="copying-address-book-entries"></a>Copiar entradas de libreta de direcciones

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Se llama al método [IABContainer::CopyEntries](iabcontainer-copyentries.md) del contenedor cuando uno o varios destinatarios del mismo contenedor u otro contenedor deben copiarse en este contenedor. **CopyEntries** tiene cuatro parámetros de entrada: una matriz de identificadores de entrada que representan los destinatarios que se van a copiar, un identificador de ventana para el indicador de progreso, un puntero de objeto de progreso y un valor de marcas. El proveedor debe mostrar el progreso si la marca AB_NO_DIALOG no está establecida y usar el objeto progress del parámetro  _lpProgress_ si no es NULL. Si  _lpProgress_ es NULL, llame a [IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md) para usar el objeto de progreso MAPI. Para obtener más información acerca de cómo mostrar el progreso, vea [Mostrar un indicador de progreso](mapi-progress-indicators.md).
  
Además de AB_NO_DIALOG suprimir un indicador de progreso, se puede establecer una de las otras dos marcas para solicitar un tipo de comprobación de entrada duplicada: CREATE_CHECK_DUP_LOOSE o CREATE_CHECK_DUP_STRICT. Las CREATE_CHECK_DUP_LOOSE y CREATE_CHECK_DUP_STRICT son solo sugerencias sobre cómo el proveedor determina las entradas duplicadas y se pueden omitir. MAPI sugiere que el proveedor implemente la compatibilidad con estas marcas de la siguiente manera.
  
|**Marca de entrada duplicada**|**Implementación sugerida**|
|:-----|:-----|
|CREATE_CHECK_DUP_LOOSE  <br/> |Compruebe si el nombre para mostrar de la entrada que se va a crear coincide con el nombre para mostrar de una entrada que ya está en el contenedor.  <br/> |
|CREATE_CHECK_DUP_STRICT  <br/> |Compruebe si el nombre para mostrar y la clave de búsqueda de la entrada que se va a crear coinciden con el nombre para mostrar y la clave de búsqueda de una entrada contenedora.  <br/> |
   
La última marca, CREATE_REPLACE, indica que la nueva entrada debe reemplazar la existente si el proveedor ha determinado que una entrada que se va a crear es un duplicado de una entrada que ya está en el contenedor. 
  
Si su proveedor es una libreta de direcciones personal, incluya la propiedad **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) en cada operación de copia. La inclusión de la tabla para mostrar detalles de un destinatario copiado permite al contenedor mostrar los detalles del destinatario en lugar de tener que llamar al contenedor original para crear la pantalla.
  
 **Para implementar IABContainer::CopyEntries**
  
1. Determine si cada identificador de entrada del parámetro  _lpEntries_ tiene un formato que el proveedor controla y, si no es así, producirá un error y devolverá MAPI_E_INVALID_ENTRYID. 
    
2. Si un identificador de entrada representa un usuario de mensajería, una lista de distribución o un contenedor que el proveedor controla:
    
1. Llama al [método IMAPISupport::OpenEntry](imapisupport-openentry.md) para abrir el destinatario correspondiente. 
    
2. Copie el destinatario en el contenedor. 
    
3. Si el identificador de entrada representa un destinatario externo:
    
1. Llama al método [IABContainer::CreateEntry del](iabcontainer-createentry.md) contenedor para crear un nuevo destinatario. 
    
2. Establece las propiedades iniciales en el nuevo destinatario.
    
4. Llame al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) del nuevo objeto para guardarlo. 
    
5. Actualice la tabla de contenido del contenedor para reflejar el nuevo destinatario. 
    
6. Llama [a IMAPISupport::Notify](imapisupport-notify.md) para enviar una notificación de tabla a clientes registrados. 
    

