---
title: Constantes (API exportadas de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 7590a30e-3fd8-7ae3-f077-c80f6cc21d7b
description: Este tema contiene definiciones de constantes para las API que Outlook exportación.
ms.openlocfilehash: 65181932b858da1b32c3fbe5fd0bd7e92ca8dc9f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319876"
---
# <a name="constants-outlook-exported-apis"></a>Constantes (API exportadas de Outlook)

Este tema contiene definiciones de constantes para las API que Outlook exportación.
  
## <a name="definitions-for-time-zone-support"></a>Definiciones de compatibilidad con zona horaria

```cpp
const ULONG TZ_MAX_RULES                    = 0x00000001;  
const BYTE  TZ_BIN_VERSION_MAJOR            = 0x02;  
const BYTE  TZ_BIN_VERSION_MINOR            = 0x01; 
const WORD  TZRULE_FLAG_RECUR_CURRENT_TZREG = 0x0001; 
const WORD  TZRULE_FLAG_EFFECTIVE_TZREG     = 0x0002; 
const WORD  TZDEFINITION_FLAG_VALID_KEYNAME = 0x0002;
```

## <a name="definitions-for-category-support"></a>Definiciones de compatibilidad con categorías

|**Constante**|**Definición**|
|:-----|:-----|
|PCAFSIF_MSGEID_IS_SEARCH_KEY  <br/> |0x00000001  <br/> |
   
## <a name="miscellaneous-dispatch-identifiers"></a>Identificadores de envío varios

Outlook expone los siguientes identificadores de distribución (dispids) para que los desarrolladores puedan usar [IDispatch::Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) para obtener acceso a la propiedad o método correspondiente, o escuchar el evento correspondiente. 
  
|**Constante asociada**|**Valor dispid**|**Descripción**|**Interfaz aplicable**|
|:-----|:-----|:-----|:-----|
|**dispidFDirty** <br/> |0xF024  <br/> |Se usa para invocar la propiedad correspondiente en un elemento para comprobar si el elemento se ha modificado pero no se ha guardado.  <br/> |Objetos de nivel de elemento  <br/> |
|**dispidShowSenderPhoto** <br/> |0xF0D0  <br/> |Se usa para invocar el método correspondiente en el explorador o inspector para especificar si se va a mostrar la imagen de un contacto, basándose en un argumento determinado.  <br/> |Explorador o inspector  <br/> |
|**dispidBeforePrint** <br/> |0xFC8E  <br/> |Se usa para controlar el evento de la **función IDispatch::Invoke** que se dispara antes de una operación de impresión.  <br/> |Aplicación  <br/> |
|**dispidEventReadComplete** <br/> |0xFC8F  <br/> |Se usa para controlar el evento de la función **IDispatch::Invoke** que se dispara cuando Outlook ha completado la lectura de las propiedades del elemento.  <br/> |Objetos de nivel de elemento  <br/> |
   
## <a name="see-also"></a>Vea también

- [API exportadas de Outlook](outlook-exported-apis.md)
- [Información sobre las API exportadas por Outlook](about-apis-exported-by-outlook.md)
- [Determinar si un elemento de Outlook se ha modificado pero no guardado (referencia auxiliar de Outlook)](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
- [Especificar si se debe mostrar la imagen de un contacto en Outlook (referencia auxiliar de Outlook)](https://msdn.microsoft.com/library/office/gg262879.aspx)
- [Los eventos disponibles y su identificadores DispId (API exportadas de Outlook)](available-events-and-their-dispids-outlook-exported-apis.md)

