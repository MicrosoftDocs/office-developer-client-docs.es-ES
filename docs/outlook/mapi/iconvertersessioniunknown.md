---
title: IConverterSession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession
api_type:
- COM
ms.assetid: 24f7a14a-aa6f-4045-054b-4a7aefef25e4
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2db55d6318cf02dd131d07b34841922e61605147
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432320"
---
# <a name="iconvertersession--iunknown"></a>IConverterSession : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Permite conversiones entre objetos MIME y mensajes MAPI. Esto puede ser útil para transportar mensajes a través de Internet.
  
|||
|:-----|:-----|
|Suministrado por:  <br/> |CLSID_IConverterSession  <br/> |
|Identificador de interfaz:  <br/> |IID_IConverterSession  <br/> |
   
## <a name="vtable-order"></a>Orden de tabla virtual

|||
|:-----|:-----|
|**[SetAdrBook](iconvertersession-setadrbook.md)** <br/> |Especifica una libreta de direcciones MAPI opcional que el convertidor de MAPI a MIME usa para resolver direcciones ambiguas al convertir un mensaje MAPI en una secuencia MIME.  <br/> |
|**[SetEncoding](iconvertersession-setencoding.md)** <br/> |Inicializa la codificación que se usará durante la conversión.  <br/> |
| *Miembro de marcador de posición*  <br/> | *No se admite ni se documenta.*  <br/> |
|**[MIMEToMAPI](iconvertersession-mimetomapi.md)** <br/> |Convierte una secuencia MIME en un mensaje MAPI.  <br/> |
|**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)** <br/> |Convierte un mensaje MAPI en una secuencia MIME.  <br/> |
| *Miembro de marcador de posición*  <br/> | *No se admite ni se documenta.*  <br/> |
| *Miembro de marcador de posición*  <br/> | *No se admite ni se documenta.*  <br/> |
| *Miembro de marcador de posición*  <br/> | *No se admite ni se documenta.*  <br/> |
|**[SetTextWrapping](iconvertersession-settextwrapping.md)** <br/> |Establece el ancho de ajuste de texto de una secuencia MIME que devuelve el convertidor **en MAPIToMIMEStm**.  <br/> |
|**[SetSaveFormat](iconvertersession-setsaveformat.md)** <br/> |Establece el formato en el que el convertidor devuelve una secuencia MIME **en MAPIToMIMEStm**.  <br/> |
| *Miembro de marcador de posición*  <br/> | *No se admite ni se documenta.*  <br/> |
|**[SetCharSet](iconvertersession-setcharset.md)** <br/> |Especifica un juego de caracteres opcional que usa el convertidor de MAPI a MIME al convertir un mensaje MAPI en una secuencia MIME.  <br/> |
   
## <a name="remarks"></a>Comentarios

Llame **a SetEncoding antes** de usar **MAPIToMIMEStm para** realizar la conversión. 
  
## <a name="see-also"></a>Consulte también



[Información sobre la API de conversión de MAPI-MIME](about-the-mapi-mime-conversion-api.md)
  
[Constantes MAPI](mapi-constants.md)

