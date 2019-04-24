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
ms.openlocfilehash: 190c4bf12c8f5aaaf8143f59239bb53fb68046f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333071"
---
# <a name="copying-address-book-entries"></a>Copiar entradas de la libreta de direcciones

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Se llama al método [IABContainer:: CopyEntries](iabcontainer-copyentries.md) del contenedor cuando uno o más destinatarios del mismo u otro contenedor se van a copiar en este contenedor. **CopyEntries** tiene cuatro parámetros de entrada: una matriz de identificadores de entrada que representan los destinatarios que se van a copiar, un identificador de ventana para el indicador de progreso, un puntero de objeto de progreso y un valor de marcas. El proveedor debería mostrar el progreso si no se establece la marca AB_NO_DIALOG y usar el objeto Progress del parámetro _lpProgress_ si no es NULL. Si _lpProgress_ es null, llame a [IMAPISupport::D oprogressdialog](imapisupport-doprogressdialog.md) para usar el objeto de progreso de MAPI. Para obtener más información acerca de cómo mostrar el progreso, vea [Mostrar un indicador de progreso](mapi-progress-indicators.md).
  
Además de AB_NO_DIALOG para suprimir un indicador de progreso, se puede establecer una de las otras dos marcas para solicitar un tipo de comprobación de entrada duplicada: CREATE_CHECK_DUP_LOOSE o CREATE_CHECK_DUP_STRICT. Los indicadores CREATE_CHECK_DUP_LOOSE y CREATE_CHECK_DUP_STRICT solo son sugerencias sobre cómo el proveedor determina las entradas duplicadas y se puede omitir. MAPI sugiere que su proveedor implemente la compatibilidad con estas marcas de la siguiente manera.
  
|**Marca de entrada duplicada**|**Implementación sugerida**|
|:-----|:-----|
|CREATE_CHECK_DUP_LOOSE  <br/> |Compruebe si el nombre para mostrar de la entrada que se va a crear coincide con el nombre para mostrar de una entrada que ya está en el contenedor.  <br/> |
|CREATE_CHECK_DUP_STRICT  <br/> |Compruebe si tanto el nombre para mostrar como la clave de búsqueda de la entrada que se va a crear coinciden con el nombre para mostrar y la clave de búsqueda de una entrada de contenedor.  <br/> |
   
La última marca, CREATE_REPLACE, indica que la nueva entrada debe reemplazar la existente si el proveedor ha determinado que una entrada que se va a crear es un duplicado de una entrada que ya se encuentra en el contenedor. 
  
Si su proveedor es una libreta personal de direcciones, incluya la propiedad **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) en cada operación de copia. La inclusión de la tabla de visualización de detalles de un destinatario copiado permite que el contenedor muestre los detalles del destinatario en lugar de tener que llamar al contenedor original para crear la visualización.
  
 **Para implementar IABContainer:: CopyEntries**
  
1. DeTermine si cada identificador de entrada en el parámetro _lpEntries_ está en un formato que el proveedor controla y, si no es así, se produce un error y se devuelve MAPI_E_INVALID_ENTRYID. 
    
2. Si un identificador de entrada representa un usuario de mensajería, una lista de distribución o un contenedor que el proveedor controla:
    
1. Llame al método [IMAPISupport:: OpenEntry](imapisupport-openentry.md) para abrir el destinatario correspondiente. 
    
2. Copie el destinatario en el contenedor. 
    
3. Si el identificador de entrada representa un destinatario externo:
    
1. Llame al método [IABContainer:: CreateEntry](iabcontainer-createentry.md) del contenedor para crear un nuevo destinatario. 
    
2. Establezca las propiedades iniciales en el nuevo destinatario.
    
4. Llame al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) del nuevo objeto para guardarlo. 
    
5. Actualice la tabla de contenido del contenedor para reflejar el nuevo destinatario. 
    
6. Llamar a [IMAPISupport:: Notify](imapisupport-notify.md) para enviar una notificación de tabla a los clientes registrados. 
    

