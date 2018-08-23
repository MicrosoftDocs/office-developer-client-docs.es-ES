---
title: Propiedad canónica PidTagAddressBookChooseDirectoryAutomatically
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cecd0679-4bc2-4399-8f89-a4e17bb909a0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b685fd0ebe4a2d0bfcfd8aab3015602b84932db7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564944"
---
# <a name="pidtagaddressbookchoosedirectoryautomatically-canonical-property"></a>Propiedad canónica PidTagAddressBookChooseDirectoryAutomatically

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Permite que Microsoft Outlook 2010 y Microsoft Outlook 2013 elegir el más adecuada lista global de direcciones (GAL) o la carpeta de contactos para el buzón de correo actual.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY  <br/> |
|Identificador:  <br/> |0x3D1C000B  <br/> |
|Tipo de propiedad:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Libreta de direcciones  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad corresponde a la opción **elija automáticamente** en el cuadro de diálogo Opciones de la libreta de direcciones. Cuando esta propiedad existe en la sección de perfil IID_CAPONE_PROF y está establecida en **true**, la libreta de direcciones diálogo ya no es el valor predeterminado es el contenedor especificado por el método [SetDefaultDir](iaddrbook-setdefaultdir.md) , pero elige una libreta de direcciones que Outlook 2010 o Outlook 2013 considere adecuado para el contexto en el que se muestra el cuadro de diálogo. Tenga en cuenta que esto puede producir una mala experiencia para los proveedores de libreta de direcciones de otros fabricantes. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapitags.h
  
> Contiene las definiciones de propiedades que se muestran como propiedades asociadas.
    
Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

