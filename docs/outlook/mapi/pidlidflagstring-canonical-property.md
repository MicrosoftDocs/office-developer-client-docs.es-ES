---
title: Propiedad canónica PidLidFlagString
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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b3cd88db7e93b53990cf0181af623ebca75f0c6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357788"
---
# <a name="pidlidflagstring-canonical-property"></a>Propiedad canónica PidLidFlagString

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un índice que identifica un conjunto de cadenas de texto predefinidas asociadas con la marca.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidFlagStringEnum  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Common  <br/> |
|IDENTIFICADOR largo (LID):  <br/> |0x000085C0  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Tarea  <br/> |
   
## <a name="remarks"></a>Comentarios

Si se establece esta propiedad, los clientes deben usar el valor de cadena correspondiente en las tablas siguientes (por ejemplo, para sustituir una cadena que se traduce al idioma del usuario actual) y deben omitir el valor establecido en **dispidFlagRequest** ([ PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) y **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)). 
  
Los valores preDeterminados que se sugieren al usuario para los objetos de contacto son los siguientes:
  
|**Value**|**Cadena en inglés**|
|:-----|:-----|
|0x00000000 o no está presente  <br/> | Siga las instrucciones relacionadas con la presentación de **dispidFlagRequest**.  <br/> |
|0x0000006E  <br/> |"Seguimiento"  <br/> |
|0x0000006F  <br/> |Call  <br/> |
|0x00000070  <br/> |"Organizar reunión"  <br/> |
|0x00000071  <br/> |"Enviar correo electrónico"  <br/> |
|0x00000072  <br/> |"Enviar carta"  <br/> |
   
Los valores preDeterminados que se sugieren al usuario para todos los demás objetos de mensaje son los siguientes:
  
|**Value**|**Cadena en inglés**|
|:-----|:-----|
|0x00000000 o no está presente  <br/> | Siga las instrucciones relacionadas con la presentación de **dispidFlagRequest**.  <br/> |
|0x00000001  <br/> |Call  <br/> |
|0x00000002  <br/> |"No reEnviar"  <br/> |
|0x00000003  <br/> |"Seguimiento"  <br/> |
|0x00000004  <br/> |"Para su información"  <br/> |
|0x00000005  <br/> |"Reenviar"  <br/> |
|0x00000006  <br/> |"No es necesario responder"  <br/> |
|0x00000007  <br/> |Sin  <br/> |
|0x00000008  <br/> |"Responder"  <br/> |
|0x00000009  <br/> |"Responder a todos"  <br/> |
|0x0000000A  <br/> |Comprueba  <br/> |
   
Todas las cadenas especificadas más arriba pueden traducirse al idioma del usuario, si procede.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones relacionadas con la marcación.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

