---
title: Acerca de la API de libre/ocupado
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 17c5e44e-ae56-8de7-3579-90171d996411
description: La API de la información de disponibilidad permite a los proveedores de correo proporcionar información de estado de disponibilidad para las cuentas de usuario especificado dentro de un intervalo de tiempo especificado.
ms.openlocfilehash: 8b1559173297fbde9930b6f8f7fbc74f176273da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816054"
---
# <a name="about-the-freebusy-api"></a>Acerca de la API de libre/ocupado

La API de la información de disponibilidad permite a los proveedores de correo proporcionar información de estado de disponibilidad para las cuentas de usuario especificado dentro de un intervalo de tiempo especificado. El estado de disponibilidad de un bloque de tiempo en el calendario de un usuario es uno de los siguientes: fuera de la oficina, ocupado, provisional o libre.
  
## <a name="create-a-freebusy-provider"></a>Crear un proveedor de libre/ocupado

Para proporcionar información de disponibilidad a los usuarios de correo, un proveedor de correo crea un proveedor de libre/ocupado y registra con Outlook. El proveedor de disponibilidad debe implementar las interfaces siguientes. Tenga en cuenta que un número de miembros en estas interfaces no es compatibles y debe devolver que valores devueltos especificado. En particular, la API de la información de disponibilidad no es compatible con acceso de escritura para la información de disponibilidad y acceso a las cuentas de delegado.
  
- [IFreeBusySupport](ifreebusysupport.md) : esta interfaz admite la especificación de las interfaces que tienen acceso a datos de disponibilidad para los usuarios especificados. Se utiliza [FBUser](fbuser.md) para identificar a un usuario. 
    
- [IFreeBusyData](ifreebusydata.md) : esta interfaz obtiene y establece un intervalo de tiempo para un usuario determinado y devuelve una interfaz para enumerar los bloques de libre/ocupado de datos dentro de este intervalo de tiempo. Tiempo relativo usa para obtener y establecer este intervalo de tiempo. Para obtener más información, vea [usar la hora relativa para tener acceso a datos de disponibilidad](how-to-use-relative-time-to-access-free-busy-data.md).
    
- [IEnumFBBlock](ienumfbblock.md) : esta interfaz admite el acceso y enumerar los bloques de disponibilidad de datos para un usuario dentro de un intervalo de tiempo. 
    
   > [!NOTE]
   > Una enumeración contiene bloques de libre/ocupado que indican el estado de disponibilidad de los períodos de tiempo en el calendario de un usuario, dentro de un intervalo de tiempo (especificado por [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)). Bloques de formulario de elementos en un calendario, como las citas y las convocatorias de reunión, en la enumeración. Se combinan los elementos que están adyacentes en el calendario y tienen el mismo estado libre/ocupado para formulario un bloque único. Un período de tiempo en un calendario libre también de formularios de un bloque. Por lo tanto, no hay dos bloques consecutivos en una enumeración tendría el mismo estado libre/ocupado. Estos bloques no se superponen en el tiempo. Cuando hay elementos superpuestos en un calendario, Outlook combina estos elementos para formar bloques de libre/ocupada no se superponen en la enumeración basándose en este orden de prioridad: fuera de la oficina, ocupado, provisional. 
  
Para registrar el proveedor de libre/ocupado con Outlook, el proveedor de correo debe hacer lo siguiente:
  
1. Registrar el proveedor de libre/ocupado con COM, proporcionar un CLSID que permite el acceso a la implementación del proveedor de **IFreeBusySupport**. 
    
2. Decirles a Outlook que existe el proveedor de la disponibilidad mediante la configuración de la clave siguiente (donde `<xx.x>` representa la versión de Outlook) en el registro del sistema: 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\<xx.x>\Outlook\SchedulingInformation\FreeBusySupport`
    
   Por ejemplo, si el proveedor de transporte es SMTP, para registrar el proveedor con Microsoft Outlook 2010, establezca la siguiente clave a los datos en la tabla siguiente: 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook\SchedulingInformation\FreeBusySupport`
    
   |Nombre |Tipo |Valor |
   |:-----|:-----|:-----|
   |SMTP  |REG_SZ  |{CLSID para implementación respectivo de IFreeBusySupport}  |
   
   En este escenario, Outlook co-autoría crea la clase COM y lo usa para recuperar información de disponibilidad de los usuarios de correo SMTP.
    
Para admitir un proveedor de libreta de direcciones y transporte de dirección que use un tipo de entrada de dirección que no sean SMTP, cambiar el *nombre* en consecuencia. 
  
> [!NOTE]
> Durante la instalación, deben comprobar proveedores de libre/ocupado si una configuración del registro para el mismo tipo de entrada de dirección ya existe. Si lo hace, el proveedor de libre/ocupado debe sobrescribir el proveedor actual para ese tipo de entrada de dirección y restaurar a ese proveedor cuando desinstala. Sin embargo, si un usuario ha instalado más de un proveedor de libre/ocupado para el mismo tipo de entrada de dirección, el usuario debe desinstalar estos proveedores en el orden inverso como instalación (es decir, desinstale el proveedor más reciente siempre). De lo contrario, el registro puede apuntar a un proveedor que ya se ha desinstalado. 
  
## <a name="api-components"></a>Componentes de la API

La API de libre/ocupado incluye los siguientes componentes:
  
### <a name="definitions"></a>Definiciones

- [Constantes (API de libre/ocupado)](constants-free-busy-api.md)
    
### <a name="data-types"></a>Tipos de datos

- [FBBlock_1](fbblock_1.md)
- [FBStatus](fbstatus.md)
- [FBUser](fbuser.md)
    
### <a name="interfaces"></a>Interfaces

- [IEnumFBBlock](ienumfbblock.md)
- [IFreeBusyData](ifreebusydata.md)
- [IFreeBusySupport](ifreebusysupport.md)
    

