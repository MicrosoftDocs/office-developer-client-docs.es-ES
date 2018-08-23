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
ms.openlocfilehash: d797932a9fd22944f1cfd78e7fb67cd3ddbf8632
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588821"
---
# <a name="synchronizing-text-and-formatting"></a>Sincronizar texto y formato

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El desafío principal en el envío de mensajes de formato de texto enriquecido (RTF) es mantener el texto sincronizado con el formato. Para asegurarse de que, cuando los mensajes llegan a su destino se hayan definido como sus creadores pensados y que el formato de texto y se sincronizan, MAPI proporciona la función [RTFSync](rtfsync.md) . **RTFSync** normalmente se llama por los clientes de tener en cuenta RTF antes de mostrar los mensajes entrantes y por la cola MAPI cuando descarga los mensajes a un proveedor de transporte. Los autores de llamadas especifican el área de discrepancia posible pasando uno o dos indicadores a **RTFSync**:
  
- RTF_SYNC_BODY_CHANGED para indicar una modificación en el texto del mensaje.
    
- RTF_SYNC_RTF_CHANGED para indicar una modificación en el formato de mensaje.
    
El proceso de sincronización que se produce en **RTFSync** es una comprobación sofisticada redundancia cíclica (CRC) del texto del mensaje que se pasa por alto algunos caracteres y convierte a otras personas. Se omiten los caracteres que se agregaron más probable es que por los proveedores de transporte. MAPI define varias propiedades para trabajar con formato RTF, tal como se describe en la siguiente tabla. 
  
|**Propiedad RTF**|**Descripción**|
|:-----|:-----|
|**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))  <br/> |Indica el principio del texto del mensaje real.  <br/> |
|**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))  <br/> |Contiene el resultado de la comprobación de redundancia cíclica del texto del mensaje.  <br/> |
|**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))  <br/> |Contiene el número de caracteres en **PR_RTF_SYNC_BODY_CRC**.  <br/> |
|**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))  <br/> |Establecer en TRUE cuando el mensaje de formato de texto y se hayan sincronizado.  <br/> |
|**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))  <br/> |Contiene el número de caracteres nonwhitespace que incluya el texto del mensaje.  <br/> |
|**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))  <br/> |Contiene el número de caracteres nonwhitespace que finalizan el texto del mensaje.  <br/> |
   

