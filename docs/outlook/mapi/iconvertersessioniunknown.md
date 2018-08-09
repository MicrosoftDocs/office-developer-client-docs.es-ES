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
ms.openlocfilehash: a89b1a93b2b03f97426a3988739e9b0d8411f113
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817180"
---
# <a name="iconvertersession--iunknown"></a>IConverterSession : IUnknown

  
  
**Hace referencia a**: Outlook 
  
Permite que las conversiones entre objetos MIME y los mensajes MAPI. Esto puede resultar útil en transportar los mensajes a través de Internet.
  
|||
|:-----|:-----|
|Suministrado por:  <br/> |CLSID_IConverterSession  <br/> |
|Identificador de interfaz:  <br/> |IID_IConverterSession  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|**[SetAdrBook](iconvertersession-setadrbook.md)** <br/> |Especifica una libreta de direcciones MAPI opcional que usa la MAPI para el convertidor MIME para resolver direcciones ambiguas Cuando se convierte un mensaje MAPI a una secuencia MIME.  <br/> |
|**[SetEncoding](iconvertersession-setencoding.md)** <br/> |Inicializa la codificación para usar durante la conversión.  <br/> |
| *Miembro de marcador de posición*  <br/> | *No se admiten o documentado.*  <br/> |
|**[MIMEToMAPI](iconvertersession-mimetomapi.md)** <br/> |Convierte una secuencia MIME en un mensaje MAPI.  <br/> |
|**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)** <br/> |Convierte un mensaje MAPI a una secuencia MIME.  <br/> |
| *Miembro de marcador de posición*  <br/> | *No se admiten o documentado.*  <br/> |
| *Miembro de marcador de posición*  <br/> | *No se admiten o documentado.*  <br/> |
| *Miembro de marcador de posición*  <br/> | *No se admiten o documentado.*  <br/> |
|**[SetTextWrapping](iconvertersession-settextwrapping.md)** <br/> |Establece el ancho de una secuencia de MIME que devuelve el convertidor en **MAPIToMIMEStm**de ajuste de texto.  <br/> |
|**[SetSaveFormat](iconvertersession-setsaveformat.md)** <br/> |Establece el formato que el convertidor devuelve una secuencia MIME en **MAPIToMIMEStm**.  <br/> |
| *Miembro de marcador de posición*  <br/> | *No se admiten o documentado.*  <br/> |
|**[SetCharSet](iconvertersession-setcharset.md)** <br/> |Especifica que la MAPI para el convertidor MIME utiliza cuando se convierte un mensaje MAPI a una secuencia MIME del conjunto de un carácter opcional.  <br/> |
   
## <a name="remarks"></a>Comentarios

Llame a **SetEncoding** antes de usar **MAPIToMIMEStm** para llevar a cabo la conversión. 
  
## <a name="see-also"></a>Vea también



[Información sobre la API de conversión de MAPI-MIME](about-the-mapi-mime-conversion-api.md)
  
[Constantes MAPI](mapi-constants.md)

