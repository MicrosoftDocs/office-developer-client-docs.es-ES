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
ms.openlocfilehash: 41fdaf333084b7d567f4e67ae9fd2638a1731349
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409667"
---
# <a name="pidtagaddressbookchoosedirectoryautomatically-canonical-property"></a>Propiedad canónica PidTagAddressBookChooseDirectoryAutomatically

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Habilita Microsoft Outlook 2010 y Microsoft Outlook 2013 para elegir la lista global de direcciones (GAL) o la carpeta de contactos más adecuada para el buzón actual.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY  <br/> |
|Identificador:  <br/> |0x3D1C000B  <br/> |
|Tipo de propiedad:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Libreta de direcciones  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad corresponde a la opción **elegir automáticamente** en el cuadro de diálogo Opciones de la libreta de direcciones. Cuando esta propiedad existe en la sección de perfil IID_CAPONE_PROF y se establece en **true**, el cuadro de diálogo libreta de direcciones ya no tiene el valor predeterminado del contenedor especificado por el método [SetDefaultDir](iaddrbook-setdefaultdir.md) , pero elige una libreta de direcciones que outlook 2010 o Outlook 2013 considera apropiado para el contexto en el que se muestra el cuadro de diálogo. Tenga en cuenta que esto puede dar como resultado una mala experiencia para los proveedores de la libreta de direcciones de otros fabricantes. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapitags. h
  
> Contiene definiciones de propiedades que se enumeran como propiedades asociadas.
    
Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Ver también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

