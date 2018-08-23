---
title: Constantes (API exportadas de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 7590a30e-3fd8-7ae3-f077-c80f6cc21d7b
description: Este tema contiene las definiciones de constantes para las API que exporta de Outlook.
ms.openlocfilehash: 8b7a9d70b2fc5d26c52a8729797221a44526360c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564468"
---
# <a name="constants-outlook-exported-apis"></a>Constantes (API exportadas de Outlook)

Este tema contiene las definiciones de constantes para las API que exporta de Outlook.
  
## <a name="definitions-for-time-zone-support"></a>Admiten las definiciones de zona horaria

```cpp
const ULONG TZ_MAX_RULES                    = 0x00000001;  
const BYTE  TZ_BIN_VERSION_MAJOR            = 0x02;  
const BYTE  TZ_BIN_VERSION_MINOR            = 0x01; 
const WORD  TZRULE_FLAG_RECUR_CURRENT_TZREG = 0x0001; 
const WORD  TZRULE_FLAG_EFFECTIVE_TZREG     = 0x0002; 
const WORD  TZDEFINITION_FLAG_VALID_KEYNAME = 0x0002;
```

## <a name="definitions-for-category-support"></a>Definiciones de soporte de categoría

|**Constante**|**Definición**|
|:-----|:-----|
|PCAFSIF_MSGEID_IS_SEARCH_KEY  <br/> |0x00000001  <br/> |
   
## <a name="miscellaneous-dispatch-identifiers"></a>Identificadores de envío varios

Outlook expone los siguientes identificadores de envío (DISPID) para que los programadores pueden utilizar [IDispatch:: Invoke](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) para obtener acceso a la propiedad correspondiente o el método o escuchar el evento correspondiente. 
  
|**Constante asociada**|**Valor de DISPID**|**Descripción**|**Interfaz aplicable**|
|:-----|:-----|:-----|:-----|
|**dispidFDirty** <br/> |0xF024  <br/> |Se usa para invocar la propiedad correspondiente en un elemento para comprobar si el elemento se ha modificado pero no se ha guardado.  <br/> |Objetos de nivel de elemento  <br/> |
|**dispidShowSenderPhoto** <br/> |0xF0D0  <br/> |Se usa para invocar el método correspondiente en el explorador o inspector para especificar si se debe mostrar la imagen de un contacto, basándose en un argumento determinado.  <br/> |El explorador o inspector  <br/> |
|**dispidBeforePrint** <br/> |0xFC8E  <br/> |Se usa para controlar el evento de la función de **IDispatch:: Invoke** que se desencadena antes de una operación de impresión.  <br/> |Aplicación  <br/> |
|**dispidEventReadComplete** <br/> |0xFC8F  <br/> |Se usa para controlar el evento de la función de **IDispatch:: Invoke** que se desencadena cuando Outlook ha finalizado la lectura de las propiedades del elemento.  <br/> |Objetos de nivel de elemento  <br/> |
   
## <a name="see-also"></a>Recursos adicionales

- [API exportadas de Outlook](outlook-exported-apis.md)
- [Información sobre las API exportadas por Outlook](about-apis-exported-by-outlook.md)
- [Determinar si un elemento de Outlook se ha modificado pero no guardado (referencia auxiliar de Outlook)](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
- [Especificar si se debe mostrar la imagen de un contacto en Outlook (referencia auxiliar de Outlook)](https://msdn.microsoft.com/en-us/library/office/gg262879.aspx)
- [Los eventos disponibles y su identificadores DispId (API exportadas de Outlook)](available-events-and-their-dispids-outlook-exported-apis.md)

