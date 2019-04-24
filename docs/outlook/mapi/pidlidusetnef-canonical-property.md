---
title: Propiedad canónica PidLidUseTnef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidUseTnef
api_type:
- COM
ms.assetid: 954048d6-e2eb-43e7-b52c-c2f047bb84a4
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 56f6e2355ee2e64cc766bafe27cd59454e210ab6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315424"
---
# <a name="pidlidusetnef-canonical-property"></a>Propiedad canónica PidLidUseTnef

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica si el formato de encapsulación neutro para el transporte (TNEF) debe incluirse en un mensaje cuando dicho mensaje se convierte de MAPI a Multipurpose Internet Mail Extensions (MIME) o protocolo simple de transferencia de correo (SMTP).
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidUseTNEF  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Common  <br/> |
|IDENTIFICADOR largo (LID):  <br/> |0x00008582  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Configuración en tiempo de ejecución  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad especifica si TNEF debe incluirse en un mensaje cuando dicho mensaje se convierte de TNEF al formato MIME o SMTP. Es posible que esta propiedad esté ausente y, si es así, TNEF no debe incluirse en el mensaje.
  
Esta propiedad sólo se aplica cuando el mensaje se envía desde una cuenta de correo POP3/SMTP y no se aplica cuando otros proveedores, como Microsoft Exchange Server, envían el mensaje.
  
En determinadas circunstancias, como cuando se habilitan los botones de votación o se adjunta un objeto OLE incrustado a un mensaje, Outlook puede establecer esta propiedad para forzar el uso de TNEF.
  
La propiedad **PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)) puede usarse para exigir únicamente texto sin formato, y no TNEF, al enviar un mensaje. Debido a que **PidLidUseTNEF** reemplaza la configuración de **PR_MSG_EDITOR_FORMAT**, una aplicación que desee forzar el texto sin formato en un mensaje saliente también debe buscar **PIDLIDUSETNEF** y restablecerla en false. Además, el complemento debe quitar las características de mensaje que requerían TNEF para evitar datos adjuntos inutilizables en el mensaje que finalmente se envían. 
  
Usar la marca **CCSF_USE_TNEF** al llamar a [IConverterSession:: MAPIToMIMEStm](iconvertersession-mapitomimestm.md) para convertir un mensaje MAPI saliente en una secuencia MIME también puede exigir TNEF. Esto es válido incluso si no se establece **PidLidUseTNEF** . 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se admiten para los objetos de mensaje de correo electrónico.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codifica y descodifica objetos de mensaje y datos adjuntos en una representación de secuencia eficaz.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

