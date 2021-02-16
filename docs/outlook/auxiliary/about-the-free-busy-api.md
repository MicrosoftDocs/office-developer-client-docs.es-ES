---
title: Información sobre la API de disponibilidad
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 17c5e44e-ae56-8de7-3579-90171d996411
description: La API de disponibilidad permite a los proveedores de correo proporcionar información de estado de disponibilidad para cuentas de usuario especificadas dentro de un intervalo de tiempo especificado.
ms.openlocfilehash: 1bcd191b57238771ede6f035216fe3997e82e03a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433762"
---
# <a name="about-the-freebusy-api"></a>Información sobre la API de disponibilidad

La API de disponibilidad permite a los proveedores de correo proporcionar información de estado de disponibilidad para cuentas de usuario especificadas dentro de un intervalo de tiempo especificado. El estado de disponibilidad de un bloque de tiempo en el calendario de un usuario es uno de los siguientes: fuera de la oficina, ocupado, provisional o gratuito.
  
## <a name="create-a-freebusy-provider"></a>Crear un proveedor de disponibilidad

Para proporcionar información de disponibilidad a los usuarios de correo, un proveedor de correo crea un proveedor de disponibilidad y lo registra con Outlook. El proveedor de disponibilidad debe implementar las siguientes interfaces. Tenga en cuenta que no se admiten varios miembros en estas interfaces y debe devolver los valores devueltos especificados. En particular, la API de disponibilidad no admite el acceso de escritura a la información de disponibilidad ni el acceso delegado a las cuentas.
  
- [IFreeBusySupport: esta](ifreebusysupport.md) interfaz admite la especificación de interfaces que tienen acceso a datos de disponibilidad para usuarios especificados. Usa [FBUser para](fbuser.md) identificar a un usuario. 
    
- [IFreeBusyData:](ifreebusydata.md) esta interfaz obtiene y establece un intervalo de tiempo para un usuario determinado y devuelve una interfaz para enumerar bloques de datos de disponibilidad dentro de este intervalo de tiempo. Usa tiempo relativo para obtener y establecer este intervalo de tiempo. Para obtener más información, vea [Usar tiempo relativo para obtener acceso a los datos de disponibilidad.](how-to-use-relative-time-to-access-free-busy-data.md)
    
- [IEnumFBBlock: esta](ienumfbblock.md) interfaz admite el acceso y la enumeración de bloques de datos de disponibilidad de un usuario dentro de un intervalo de tiempo. 
    
   > [!NOTE]
   > Una enumeración contiene bloques de disponibilidad que indican el estado de disponibilidad de períodos de tiempo en el calendario de un usuario, dentro de un intervalo de tiempo (especificado por [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)). Elementos de un calendario, como citas y solicitudes de reunión, bloques de formulario en la enumeración. Los elementos adyacentes entre sí en el calendario y que tienen el mismo estado de disponibilidad se combinan para formar un único bloque. Un período de tiempo libre en un calendario también forma un bloque. Por lo tanto, no hay dos bloques consecutivos en una enumeración que tengan el mismo estado de disponibilidad. Estos bloques no se superponen en el tiempo. Cuando hay elementos superpuestos en un calendario, Outlook combina estos elementos para formar bloques de disponibilidad no superpuestos en la enumeración en función de este orden de prioridad: fuera de la oficina, ocupado, provisional. 
  
Para registrar el proveedor de disponibilidad con Outlook, el proveedor de correo debe hacer lo siguiente:
  
1. Registre el proveedor de disponibilidad con COM, proporcionando un CLSID que permite el acceso a la implementación del proveedor de **IFreeBusySupport**. 
    
2. Para que Outlook sepa que existe el proveedor de disponibilidad, establece la siguiente clave (donde representa la versión de `<xx.x>` Outlook) en el Registro del sistema: 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\<xx.x>\Outlook\SchedulingInformation\FreeBusySupport`
    
   Por ejemplo, si el proveedor de transporte es SMTP, para registrar el proveedor con Microsoft Outlook 2010, establezca la siguiente clave para los datos de la tabla siguiente: 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook\SchedulingInformation\FreeBusySupport`
    
   |Nombre |Tipo |Valor |
   |:-----|:-----|:-----|
   |SMTP  |REG_SZ  |{CLSID para la implementación respectiva de IFreeBusySupport}  |
   
   En este escenario, Outlook crea en co-crea la clase COM y la usa para recuperar información de disponibilidad de cualquier usuario de correo SMTP.
    
Para admitir una libreta de direcciones y un proveedor de transporte que usen un tipo de entrada de dirección distinto de SMTP, cambie el  *nombre* en consecuencia. 
  
> [!NOTE]
> Durante la instalación, los proveedores de disponibilidad deben comprobar si ya existe una configuración del Registro para el mismo tipo de entrada de dirección. Si es así, el proveedor de disponibilidad debe sobrescribir el proveedor actual para ese tipo de entrada de dirección y restaurarlo cuando se desinstala. Sin embargo, si un usuario ha instalado más de un proveedor de disponibilidad para el mismo tipo de entrada de dirección, el usuario debe desinstalar estos proveedores en el orden inverso como instalación (es decir, desinstalar siempre el proveedor más reciente). De lo contrario, el Registro puede apuntar a un proveedor que ya se ha desinstalado. 
  
## <a name="api-components"></a>Componentes de api

La API de disponibilidad incluye los siguientes componentes:
  
### <a name="definitions"></a>Definiciones

- [Constantes (API de disponibilidad)](constants-free-busy-api.md)
    
### <a name="data-types"></a>Tipos de datos

- [FBBlock_1](fbblock_1.md)
- [FBStatus](fbstatus.md)
- [FBUser](fbuser.md)
    
### <a name="interfaces"></a>Interfaces

- [IEnumFBBlock](ienumfbblock.md)
- [IFreeBusyData](ifreebusydata.md)
- [IFreeBusySupport](ifreebusysupport.md)
    

