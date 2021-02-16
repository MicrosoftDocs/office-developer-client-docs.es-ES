---
title: Propiedad canónica PidLidPostalAddressId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidPostalAddressId
api_type:
- COM
ms.assetid: 30fdfb20-1e12-442a-bfa0-8c18c15fa5c3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 83f3c0559a3317de3789f8c93d024f08ada3e735
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315998"
---
# <a name="pidlidpostaladdressid-canonical-property"></a>Propiedad canónica PidLidPostalAddressId

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica qué dirección física es la dirección postal del contacto.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidPostalAddressId  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Address  <br/> |
|Long ID (LID):  <br/> |0x00008022  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Contacto  <br/> |
   
## <a name="remarks"></a>Comentarios

Si está presente, esta propiedad debe tener uno de los valores especificados en la tabla siguiente o en [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx). Si no se establece, la aplicación debe suponer que el valor es "0x00000000".
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0x00000000  <br/> |No se selecciona ninguna dirección como dirección postal. **PR_STREET_ADDRESS** ([PidTagStreetAddress](pidtagstreetaddress-canonical-property.md)), **PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md)), **PR_STATE_OR_PROVINCE** ([PidTagStateOrProvince](pidtagstateorprovince-canonical-property.md)), **PR_POSTAL_CODE** ([PidTagPostalCode](pidtagpostalcode-canonical-property.md)), **PR_COUNTRY** ([PidTagCountry](pidtagcountry-canonical-property.md)), **dispidAddressCountryCode** ([PidLidAddressCountryCode](pidlidaddresscountrycode-canonical-property.md)) y **PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md)) no deben establecerse todos.  <br/> |
|0x00000001  <br/> |La dirección principal es la dirección postal. Los valores de las propiedades **PR_STREET_ADDRESS**, **PR_LOCALITY**, **PR_STATE_OR_PROVINCE**, **PR_POSTAL_CODE**, **PR_POST_OFFICE_BOX** ([PidTagPostOfficeBox](pidtagpostofficebox-canonical-property.md)), **PR_COUNTRY**, **dispidAddressCountryCode** y PR_POSTAL_ADDRESS deben ser iguales **a** los valores de las propiedades **PR_HOME_ADDRESS_STREET** ([PidTagHomeAddressStreet](pidtaghomeaddressstreet-canonical-property.md)), **PR_HOME_ADDRESS_CITY** ([PidTagHomeAddressCity](pidtaghomeaddresscity-canonical-property.md)), **PR_HOME_ADDRESS_STATE_OR_PROVINCE** ([PidTagHomeAddressStateOrProvince](pidtaghomeaddressstateorprovince-canonical-property.md)), **PR_HOME_ADDRESS_POSTAL_CODE** ([PidTagHomeAddressPostalCode](pidtaghomeaddresspostalcode-canonical-property.md)), **PR_HOME_ADDRESS_POST_OFFICE_BOX** ([PidTagHomeAddressPostOfficeBox](pidtaghomeaddresspostofficebox-canonical-property.md)), **PR_HOME_ADDRESS_COUNTRY** ([PidTagHomeAddressCountry](pidtaghomeaddresscountry-canonical-property.md)), **dispidHomeAddressCountryCode** ([PidLidHomeAddressCountryCode](pidlidhomeaddresscountrycode-canonical-property.md)) y **dispidHomeAddress** ([PidLidHomeAddress](pidlidhomeaddress-canonical-property.md)) respectivamente.  <br/> |
|0x00000002  <br/> |La dirección de trabajo es la dirección postal. Los valores de las propiedades **PR_STREET_ADDRESS**, **PR_LOCALITY**, **PR_STATE_OR_PROVINCE**, **PR_POSTAL_CODE**, **PR_POST_OFFICE_BOX**, **PR_COUNTRY**, **dispidAddressCountryCode** y PR_POSTAL_ADDRESS deben ser iguales **a** los valores de **dispidWorkAddressStreet** ([PidLidWorkAddressStreet](pidlidworkaddressstreet-canonical-property.md)), **dispidWorkAddressCity** ([PidLidWorkAddressCity](pidlidworkaddresscity-canonical-property.md)), **dispidWorkAddressState** ([Pid PropiedadesLidWorkAddressState](pidlidworkaddressstate-canonical-property.md)), **dispidWorkAddressPostalCode** ([PidLidWorkAddressPostalCode](pidlidworkaddresspostalcode-canonical-property.md)), **dispidWorkAddressPostOfficeBox** ([PidLidWorkAddressPostOfficeBox](pidlidworkaddresspostofficebox-canonical-property.md)), **dispidWorkAddressCountry** ([PidLidWorkAddressCountry](pidlidworkaddresscountry-canonical-property.md)), **dispidWorkAddressCountryCode** ([PidLidWorkAddressCountryCode](pidlidworkaddresscountrycode-canonical-property.md)) y **dispidWorkAddress** ([PidLidWorkAddress](pidlidworkaddress-canonical-property.md)) respectivamente.  <br/> |
|0x00000003  <br/> |La otra dirección es la dirección postal. Los valores de las propiedades **PR_STREET_ADDRESS**, **PR_LOCALITY**, **PR_STATE_OR_PROVINCE**, **PR_POSTAL_CODE**, **PR_POST_OFFICE_BOX**, **PR_COUNTRY**, **dispidAddressCountryCode** y **PR_POSTAL_ADDRESS** deben ser iguales a los valores de **las** propiedades PR_OTHER_ADDRESS_STREET ([PidTagOtherAddressStreet](pidtagotheraddressstreet-canonical-property.md)), **PR_OTHER_ADDRESS_CITY** ([PidTagOtherAddressCity](pidtagotheraddresscity-canonical-property.md)), **PR_OTHER_ADDRESS_STATE_OR_PROVINCE** ([PidTagOtherAddressStateOrProvince](pidtagotheraddressstateorprovince-canonical-property.md)), **PR_OTHER_ADDRESS_POSTAL_CODE** ([PidTagOtherAddressPostalCode](pidtagotheraddresspostalcode-canonical-property.md)), **PR_OTHER_ADDRESS_POST_OFFICE_BOX** ([PidTagOtherAddressPostOfficeBox](pidtagotheraddresspostofficebox-canonical-property.md)), **dispidOtherAddressCountryCode** ([PidLidOtherAddressCountryCode](pidlidotheraddresscountrycode-canonical-property.md)) y **dispidOtherAddress** ([PidLidOtherAddress](pidlidotheraddress-canonical-property.md)) properties, respectivamente.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones permitidas para contactos y listas de distribución personales.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

