---
title: Propiedad canónica PidTagAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccount
api_type:
- HeaderDef
ms.assetid: bec199b5-abfd-4686-ad59-21092212e1a5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2962f973aa87b88f237ded69573df9ef312a7bc5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359783"
---
# <a name="pidtagaccount-canonical-property"></a>Propiedad canónica PidTagAccount

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el nombre de cuenta del destinatario. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ACCOUNT, PR_ACCOUNT_A, PR_ACCOUNT_W  <br/> |
|Identificador:  <br/> |0x3A00  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Libreta de direcciones  <br/> |
   
## <a name="remarks"></a>Comentarios

Estas propiedades proporcionan información de identificación y acceso para un destinatario. El destinatario y su organización los definen.
  
Estas propiedades normalmente contienen el nombre de correo electrónico del destinatario, es decir, el componente final de la dirección de correo electrónico, que identifica de forma única al destinatario en la organización local. El nombre del correo electrónico corresponde al nombre distintivo X.400, que está diseñado para ser un nombre corto que se garantiza que es único dentro de un dominio de mensajería determinado.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones permitidas para contactos y listas de distribución personales.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones de listas de usuarios, contactos, grupos y recursos.
    
### <a name="header-files"></a>Archivos de encabezado

mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas.
    
mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[IMailUser : IMAPIProp](imailuserimapiprop.md)


[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

