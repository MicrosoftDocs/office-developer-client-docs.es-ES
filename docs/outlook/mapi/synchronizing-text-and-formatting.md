---
title: Sincronizar texto y formato
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d7e166f0-1214-4571-b9a8-366960772a7a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 852ef988566ade8fca6551bea0d618199319d1d4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435106"
---
# <a name="synchronizing-text-and-formatting"></a>Sincronizar texto y formato

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El desafío principal de enviar mensajes con formato de texto enriquecido (RTF) es mantener el texto sincronizado con el formato. Para asegurarse de que cuando los mensajes llegan a su destino son como sus originadores y que el texto y el formato están sincronizados, MAPI proporciona la función [RTFSync](rtfsync.md) . Los clientes que reconocen RTF suelen llamar a **RTFSync** antes de mostrar los mensajes entrantes y de la cola de impresión MAPI cuando descarga mensajes a un proveedor de transporte. Los autores de las llamadas especifican el área de posible discrepancia pasando una o dos marcas a **RTFSync**:
  
- RTF_SYNC_BODY_CHANGED para indicar una modificación en el texto del mensaje.
    
- RTF_SYNC_RTF_CHANGED para indicar una modificación en el formato del mensaje.
    
El proceso de sincronización que se produce en **RTFSync** es una sofisticada comprobación de redundancia cíclica (CRC) del texto del mensaje que ignora algunos caracteres y convierte a otros. Se omiten los caracteres que más probabilidades han agregado los proveedores de transporte. MAPI define varias propiedades para trabajar con RTF como se describe en la tabla siguiente. 
  
|**Propiedad RTF**|**Descripción**|
|:-----|:-----|
|**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))  <br/> |Indica el principio del texto real del mensaje.  <br/> |
|**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))  <br/> |Contiene el resultado de la comprobación de redundancia cíclica del texto del mensaje.  <br/> |
|**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))  <br/> |Contiene el número de caracteres en **PR_RTF_SYNC_BODY_CRC**.  <br/> |
|**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))  <br/> |Se establece en TRUE cuando se han sincronizado el texto y el formato del mensaje.  <br/> |
|**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))  <br/> |Contiene el número de caracteres nonwhitespace que preceden al texto del mensaje.  <br/> |
|**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))  <br/> |Contiene el número de caracteres nonwhitespace que finalizan el texto del mensaje.  <br/> |
   

