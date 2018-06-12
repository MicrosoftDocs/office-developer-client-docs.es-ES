---
title: Propiedad canónico PidLidFlagString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFlagString
api_type:
- COM
ms.assetid: 4cf1e08b-c869-4965-a1e4-512a0684700f
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 53fe309fb15807ad698fef5a06781e5c3e0bae0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818738"
---
# <a name="pidlidflagstring-canonical-property"></a>Propiedad canónico PidLidFlagString

  
  
**Se aplica a**: Outlook 
  
Contiene un índice que identifica un conjunto predefinido de cadenas de texto asociado con la marca.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidFlagStringEnum  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Common  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x000085C0  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Tarea  <br/> |
   
## <a name="remarks"></a>Notas

Si se establece esta propiedad, los clientes deben usar el valor de cadena correspondiente en las tablas siguientes (por ejemplo, para sustituir una cadena que se convierte en el actual idioma del usuario) y deben omitir el valor establecido en **dispidFlagRequest** ([ PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) y **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)). 
  
Valores predeterminados sugeridos para el usuario para los objetos de contacto son los siguientes:
  
|**Valor**|**Cadena en inglés**|
|:-----|:-----|
|0 x 00000000 o no está presente  <br/> | Siga las instrucciones relacionados con la presentación **dispidFlagRequest**.  <br/> |
|0x0000006E  <br/> |"Seguimiento"  <br/> |
|0x0000006F  <br/> |"Llamada"  <br/> |
|0 x 00000070  <br/> |"Organizar reuniones"  <br/> |
|0 x 00000071  <br/> |"Enviar correo electrónico"  <br/> |
|0x00000072  <br/> |"Enviar carta"  <br/> |
   
Valores predeterminados de sugeridas para el usuario para todos los demás objetos de mensaje son los siguientes:
  
|**Valor**|**Cadena en inglés**|
|:-----|:-----|
|0 x 00000000 o no está presente  <br/> | Siga las instrucciones relacionados con la presentación **dispidFlagRequest**.  <br/> |
|0x00000001  <br/> |"Llamada"  <br/> |
|0x00000002  <br/> |"No reenviar"  <br/> |
|0 x 00000003  <br/> |"Seguimiento"  <br/> |
|0 x 00000004  <br/> |"Para la información de"  <br/> |
|0 x 00000005  <br/> |"Hacia adelante"  <br/> |
|0 x 00000006  <br/> |"Sin necesidad de respuesta"  <br/> |
|0 x 00000007  <br/> |"Lectura"  <br/> |
|0 x 00000008  <br/> |"Respuesta"  <br/> |
|0 x 00000009  <br/> |"Responder a todos"  <br/> |
|0x0000000A  <br/> |"Revisión"  <br/> |
   
Todas las cadenas especificadas anteriormente pueden convertirse en el idioma del usuario, si es necesario.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones relacionadas con marcas.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Ver también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedad canónico a nombres de MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI para nombres canónicos (propiedad)](mapping-mapi-names-to-canonical-property-names.md)

