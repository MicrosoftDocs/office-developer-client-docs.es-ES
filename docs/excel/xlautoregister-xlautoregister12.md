---
title: xlAutoRegister/xlAutoRegister12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRegister
keywords:
- xlautoregister (función) [excel 2007]
localization_priority: Normal
ms.assetid: aa4673cf-8e97-4678-b8d4-6a74426334f9
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e6430a54b0c0ed3b6e08d3c9256cae7dcde926ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19815715"
---
# <a name="xlautoregisterxlautoregister12"></a>xlAutoRegister/xlAutoRegister12

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Excel llama a la [función xlAutoRegister](xlautoregister-xlautoregister12.md) cada vez que se ha realizado una llamada a la función XLM **registrar**o la [función xlfRegister](xlfregister-form-1.md)de API de C equivalente, con los tipos de devolución y el argumento de la función que se está registrando que faltan. Permite que los XLL buscar sus listas internas de funciones exportadas y comandos para registrar la función con el argumento y devolver los tipos especificados.
  
Iniciar en Excel 2007, Excel llama a la función **xlAutoRegister12** preferencia a la función **xlAutoRegister** si lo exporta el XLL. 
  
Excel no requiere un XLL implementar y exportar a cualquiera de estas funciones.
  
> [!NOTE]
> Si **xlAutoRegister**/ **xlAutoRegister12** intenta registrar la función sin proporcionar el argumento y tipos de valores devueltos, produce un bucle llamada recursiva que finalmente desbordamientos de la pila de llamadas y bloquea Excel. 
  
```cs
LPXLOPER12 WINAPI xlAutoRegister12(LPXLOPER12 pxName);
LPXLOPER WINAPI xlAutoRegister(LPXLOPER pxName);
```

## <a name="parameters"></a>Parámetros

 _pxName_ (**xltypeStr**)
  
El nombre de la función XLL que se está registrando.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

La función debe devolver el resultado del intento de registrar la función XLL _pxName_ mediante la función **xlfRegister** . Si la función especificada no es una de las exportaciones de XLL, debe devolver el **#VALUE!** error, o **NULL** que Excel interpretará en **#VALUE!**.
  
## <a name="remarks"></a>Comentarios

Su implementación de **xlAutoRegister** debe realizar una búsqueda a través de listas interno de los XLL de las funciones y comandos que exporta busca una coincidencia con el nombre pasado entre mayúsculas y minúsculas. Si se encuentra la función o el comando, **xlAutoRegister** debe intentar registrarlo, mediante la función **xlfRegister** , asegurándose de proporcionar la cadena que indica los tipos de retorno y el argumento de la función, así como cualquier otro necesarios a Excel información sobre la función. A continuación, debe devolver a Excel todo lo que devuelve la llamada a **xlfRegister** . Si la función se ha registrado correctamente, **xlfRegister** devuelve un valor de **xltypeNum** que contiene el identificador de registro de la función. 
  
### <a name="example"></a>Ejemplo

Consulte el archivo `SAMPLES\EXAMPLE\EXAMPLE.C` para una implementación de ejemplo de esta función. 
  
## <a name="see-also"></a>Vea también



[REGISTRAR](xlfregister-form-1.md)
  
[ANULAR EL REGISTRO](xlfunregister-form-1.md)

