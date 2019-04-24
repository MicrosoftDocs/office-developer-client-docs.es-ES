---
title: Establecer las opciones de la libreta de direcciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9bd31233-fc8d-4e0a-9f1b-218c5ecb6d1b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f72c916e917543b11089f8f5ef1aa4b9552a1b6a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351411"
---
# <a name="setting-address-book-options"></a>Establecer las opciones de la libreta de direcciones

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Puede establecer tres propiedades que describen las opciones de uso de la libreta de direcciones:
  
- **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))
    
    La propiedad **PR_AB_SEARCH_PATH** se usa en [IAddrBook:: ResolveName](iaddrbook-resolvename.md) para determinar los contenedores que deben participar en la resolución de nombres y el orden en que deben estar involucrados. Para cada contenedor en **PR_AB_SEARCH_PATH**, **IAddrBook:: ResolveName** llama a su método [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) . Los contenedores al principio de **PR_AB_SEARCH_PATH** se buscan antes de los contenedores al final de **PR_AB_SEARCH_PATH**. 
    
    El orden de búsqueda en **PR_AB_SEARCH_PATH** se especifica mediante una estructura [SRowSet](srowset.md) , la misma estructura que se usa para representar las filas de una tabla. Para ver la ruta de acceso de búsqueda actual, puede llamar al método [IAddrBook:: GetSearchPath](iaddrbook-getsearchpath.md) y cambiarla mediante una llamada al método [IAddrBook:: SetSearchPath](iaddrbook-setsearchpath.md) . 
    
- **PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))
    
    La propiedad **PR_AB_DEFAULT_DIR** es el identificador de entrada del contenedor de libretas de direcciones que se muestra inicialmente cuando se muestra la libreta de direcciones. La configuración predeterminada del directorio permanece en vigor hasta que se cambie mediante una llamada al método [IAddrBook:: SetDefaultDir](iaddrbook-setdefaultdir.md) . Puede ver el directorio predeterminado llamando al método [IAddrBook:: GetDefaultDir](iaddrbook-getdefaultdir.md) . 
    
- **PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))
    
Estas tres propiedades son especiales porque no se puede trabajar con ellas mediante los métodos **IMAPIProp** estándar. En su lugar, debe usar los métodos **IAddrBook** . Debido a que ninguna de estas propiedades se puede cambiar con **IMAPIProp:: SetProps**, no es necesario llamar a **IMAPIProp:: SaveChanges** para realizar cambios permanentes. Las modificaciones realizadas a través de los métodos **IAddrBook** se aplican de forma inmediata. 
  
## <a name="see-also"></a>Vea también



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

