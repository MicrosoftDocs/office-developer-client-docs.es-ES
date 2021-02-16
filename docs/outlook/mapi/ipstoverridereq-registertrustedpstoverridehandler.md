---
title: IPSTOVERRIDEREQRegisterTrustedPSTOverrideHandler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDEREQ.RegisterTrustedPSTOverrideHandler
api_type:
- COM
ms.assetid: 4a73c77c-7e32-4302-bffe-a1ea13574731
description: 'Última modificación: 24 de febrero de 2013'
ms.openlocfilehash: acc0986dd80b549b0cb2b941a6937d47a4a959fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279538"
---
# <a name="ipstoverridereqregistertrustedpstoverridehandler"></a>IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Inicia el procedimiento de desbloqueo de un archivo de carpetas personales (.pst).
  
```cpp
HRESULT RegisterTrustedPSTOverrideHandler (
  LPCWSTR pwzDllPath, 
  LPVOID pvClientData
); 

```

## <a name="parameters"></a>Parámetros

 _pwzDllPath_
  
> [entrada] Puntero a la ruta de acceso de una biblioteca de vínculos dinámicos (DLL) de terceros.
    
 _pvClientData_
  
> [entrada] Un puntero a los datos de cliente, que pasará el proveedor de PST en llamadas posteriores a la función HrTrustedPSTOverrideHandlerCallback del DLL. La DLL puede usar estos datos de cliente para ayudar a comprobar si el archivo PST debe desbloquearse.
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> La llamada a la función se ha realizado correctamente.
    
## <a name="remarks"></a>Comentarios

La DLL especificada por el parámetro wzDllPath debe firmarse con un certificado digital. La DLL también debe exportar una función con la firma siguiente.
  
```
extern "C" HRESULT __cdecl HrTrustedPSTOverrideHandlerCallback(IMsgStore *pmstore, IUnknown *pOverride, LPVOID pvClientData)
```

Se llamará a esta función con un puntero al objeto IMsgStore para el PST, un puntero a un objeto IUnknown que implementa la interfaz IPSTOVERRIDE1 y un puntero a los datos suministrados originalmente a través de pvClientData.
  
Para obtener más información, vea Cómo implementar un controlador de reemplazo de PST para omitir la directiva [PSTDisableGrow en Outlook 2007](https://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>Consulte también



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

