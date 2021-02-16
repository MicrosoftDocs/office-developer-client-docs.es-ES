---
title: Leer y analizar un patrón de periodicidad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 75113097-b3ae-4d20-9796-85c62a592ef0
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c226fe79fd002cda3c557fc8416c25f98ad33626
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345930"
---
# <a name="read-and-parse-a-recurrence-pattern"></a>Leer y analizar un patrón de periodicidad
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI puede usarse para leer y analizar un patrón de periodicidad para una cita.
  
Para obtener información sobre cómo descargar, ver y ejecutar el código del proyecto de aplicación MFCMAPI al que se hace referencia en este tema, vea Instalar los ejemplos usados [en esta sección.](how-to-install-the-samples-used-in-this-section.md)

### <a name="to-parse-a-recurrence-blob"></a>Para analizar un blob de periodicidad

1. Abra un elemento de cita. Para obtener información acerca de cómo abrir un mensaje, vea [Abrir un mensaje.](opening-a-message.md)
    
2. Recuperar la propiedad con nombre **dispidApptRecur** ([PidLidAppointmentRecur Canonical Property](pidlidappointmentrecur-canonical-property.md)). Para obtener información acerca de la recuperación de propiedades con nombre, vea [propiedades con nombre MAPI](mapi-named-properties.md).
    
3. Siga las instrucciones de [[MS-OXOCAL]](https://msdn.microsoft.com/library/cc425490%28EXCHG.80%29.aspx) para leer la estructura del patrón de periodicidad de citas. 
    
La aplicación de referencia MFCMAPI muestra el último paso con la función en el archivo de origen  `BinToAppointmentRecurrencePatternStruct` InterpretProp2.cpp del proyecto MFCMapi. La  `BinToAppointmentRecurrencePatternStruct` función toma un puntero a un búfer en la memoria como parámetro. La aplicación MFCMAPI obtiene este búfer asignando primero la propiedad con nombre **dispidApptRecur** a una etiqueta de propiedad y, a continuación, solicitando el valor de la propiedad mediante el método [IMAPIProp::GetProps.](imapiprop-getprops.md) Si la propiedad es demasiado grande para recuperarla mediante el método **GetProps,** MFCMAPI abre una interfaz de secuencia para recuperar la propiedad mediante el método [IMAPIProp::OpenProperty.](imapiprop-openproperty.md) A continuación, la aplicación MFCMAPI lee los datos fuera de la secuencia para crear el búfer. 
  
Para obtener información sobre el formato del búfer, vea la propiedad [canónica PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md). La mayor parte de los datos del búfer consta de campos de un número fijo de bytes, que se deben leer uno tras otro. Algunos campos solo están presentes si otros contienen ciertos valores y el tamaño de algunos campos puede depender del valor de otros campos. Analizar el búfer para leer los distintos campos implica una gran cantidad de contabilidad. MFCMAPI usa una clase auxiliar interna denominada  `CBinaryParser` para encapsular esta contabilidad. Por ejemplo, la función comprueba si quedan suficientes bytes en el búfer para leer un DWORD y, a continuación, lee el valor y  `CBinaryParser::GetDWORD` actualiza los punteros. 
  
Después de analizar el búfer en una estructura, la aplicación MFCMAPI usa la función para convertir la estructura en una cadena para mostrarla  `AppointmentRecurrencePatternStructToString` al usuario. No se trata de la misma cadena que mostraría Outlook, sino de una vista sin procesar de los datos sobre los que Outlook crea su lógica. 
  
Es posible encontrar un búfer que contenga datos dañados o más datos de los necesarios para codificar un patrón de periodicidad. Para ayudar a identificar estos escenarios, la aplicación MFCMAPI realiza un seguimiento de la cantidad de datos que se han analizado correctamente y cuánto permanece en el búfer. Si los datos permanecen en el búfer una vez completado el análisis, MFCMAPI incluye estos "datos no deseados" en la estructura para que se puedan examinar.
  
A continuación se muestra la lista completa de la  `BinToAppointmentRecurrencePatternStruct` función. 
  
```cpp
AppointmentRecurrencePatternStruct* BinToAppointmentRecurrencePatternStruct(ULONG cbBin, LPBYTE lpBin)
{
   if (!lpBin) return NULL;
   AppointmentRecurrencePatternStruct arpPattern = {0};
   CBinaryParser Parser(cbBin,lpBin);
   size_t cbBinRead = 0;
   arpPattern.RecurrencePattern = BinToRecurrencePatternStruct(cbBin,lpBin,&cbBinRead);
   Parser.Advance(cbBinRead);
   Parser.GetDWORD(&arpPattern.ReaderVersion2);
   Parser.GetDWORD(&arpPattern.WriterVersion2);
   Parser.GetDWORD(&arpPattern.StartTimeOffset);
   Parser.GetDWORD(&arpPattern.EndTimeOffset);
   Parser.GetWORD(&arpPattern.ExceptionCount);
   if (arpPattern.ExceptionCount &&
      arpPattern.ExceptionCount == arpPattern.RecurrencePattern->ModifiedInstanceCount &&
      arpPattern.ExceptionCount < _MaxExceptions)
   {
      arpPattern.ExceptionInfo = new ExceptionInfoStruct[arpPattern.ExceptionCount];
      if (arpPattern.ExceptionInfo)
      {
         memset(arpPattern.ExceptionInfo,0,sizeof(ExceptionInfoStruct) * arpPattern.ExceptionCount);
         WORD i = 0;
         for (i = 0 ; i < arpPattern.ExceptionCount ; i++)
         {
            Parser.GetDWORD(&arpPattern.ExceptionInfo[i].StartDateTime);
            Parser.GetDWORD(&arpPattern.ExceptionInfo[i].EndDateTime);
            Parser.GetDWORD(&arpPattern.ExceptionInfo[i].OriginalStartDate);
            Parser.GetWORD(&arpPattern.ExceptionInfo[i].OverrideFlags);
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBJECT)
            {
               Parser.GetWORD(&arpPattern.ExceptionInfo[i].SubjectLength);
               Parser.GetWORD(&arpPattern.ExceptionInfo[i].SubjectLength2);
               if (arpPattern.ExceptionInfo[i].SubjectLength2 && arpPattern.ExceptionInfo[i].SubjectLength2 + 1 
                  == arpPattern.ExceptionInfo[i].SubjectLength)
               {
                  Parser.GetStringA(arpPattern.ExceptionInfo[i].SubjectLength2,&arpPattern.ExceptionInfo[i].Subject);
               }
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_MEETINGTYPE)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].MeetingType);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_REMINDERDELTA)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].ReminderDelta);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_REMINDER)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].ReminderSet);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_LOCATION)
            {
               Parser.GetWORD(&arpPattern.ExceptionInfo[i].LocationLength);
               Parser.GetWORD(&arpPattern.ExceptionInfo[i].LocationLength2);
               if (arpPattern.ExceptionInfo[i].LocationLength2 && arpPattern.ExceptionInfo[i].LocationLength2 
                  + 1 == arpPattern.ExceptionInfo[i].LocationLength)
               {
                  Parser.GetStringA(arpPattern.ExceptionInfo[i].LocationLength2,&arpPattern.ExceptionInfo[i].Location);
               }
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_BUSYSTATUS)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].BusyStatus);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_ATTACHMENT)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].Attachment);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBTYPE)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].SubType);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_APPTCOLOR)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].AppointmentColor);
            }
         }
      }
   }
   Parser.GetDWORD(&arpPattern.ReservedBlock1Size);
   if (arpPattern.ReservedBlock1Size && arpPattern.ReservedBlock1Size < _MaxReservedBlock)
   {
      Parser.GetBYTES(arpPattern.ReservedBlock1Size,&arpPattern.ReservedBlock1);
   }
   if (arpPattern.ExceptionCount &&
      arpPattern.ExceptionCount == arpPattern.RecurrencePattern->ModifiedInstanceCount &&
      arpPattern.ExceptionCount < _MaxExceptions &&
      arpPattern.ExceptionInfo)
   {
      arpPattern.ExtendedException = new ExtendedExceptionStruct[arpPattern.ExceptionCount];
      if (arpPattern.ExtendedException)
      {
         memset(arpPattern.ExtendedException,0,sizeof(ExtendedExceptionStruct) * arpPattern.ExceptionCount);
         WORD i = 0;
         for (i = 0 ; i < arpPattern.ExceptionCount ; i++)
         {
            if (arpPattern.WriterVersion2 >= 0x0003009)
            {
               Parser.GetDWORD(&arpPattern.ExtendedException[i].ChangeHighlight.ChangeHighlightSize);
               Parser.GetDWORD(&arpPattern.ExtendedException[i].ChangeHighlight.ChangeHighlightValue);
               if (arpPattern.ExtendedException[i].ChangeHighlight.ChangeHighlightSize > sizeof(DWORD))
               {
                  Parser.GetBYTES(arpPattern.ExtendedException[i].ChangeHighlight.ChangeHighlightSize 
                     - sizeof(DWORD),&arpPattern.ExtendedException[i].ChangeHighlight.Reserved);
               }
            }
            Parser.GetDWORD(&arpPattern.ExtendedException[i].ReservedBlockEE1Size);
            if (arpPattern.ExtendedException[i].ReservedBlockEE1Size &&
                arpPattern.ExtendedException[i].ReservedBlockEE1Size < _MaxReservedBlock)
            {
               Parser.GetBYTES(arpPattern.ExtendedException[i].ReservedBlockEE1Size,&arpPattern.ExtendedException[i].ReservedBlockEE1);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBJECT ||
               arpPattern.ExceptionInfo[i].OverrideFlags & ARO_LOCATION)
            {
               Parser.GetDWORD(&arpPattern.ExtendedException[i].StartDateTime);
               Parser.GetDWORD(&arpPattern.ExtendedException[i].EndDateTime);
               Parser.GetDWORD(&arpPattern.ExtendedException[i].OriginalStartDate);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBJECT)
            {
               Parser.GetWORD(&arpPattern.ExtendedException[i].WideCharSubjectLength);
               if (arpPattern.ExtendedException[i].WideCharSubjectLength)
               {
                  Parser.GetStringW(arpPattern.ExtendedException[i].WideCharSubjectLength,&arpPattern.ExtendedException[i].WideCharSubject);
               }
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_LOCATION)
            {
               Parser.GetWORD(&arpPattern.ExtendedException[i].WideCharLocationLength);
               if (arpPattern.ExtendedException[i].WideCharLocationLength)
               {
                  Parser.GetStringW(arpPattern.ExtendedException[i].WideCharLocationLength,&arpPattern.ExtendedException[i].WideCharLocation);
               }
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBJECT ||
               arpPattern.ExceptionInfo[i].OverrideFlags & ARO_LOCATION)
            {
               Parser.GetDWORD(&arpPattern.ExtendedException[i].ReservedBlockEE2Size);
               if (arpPattern.ExtendedException[i].ReservedBlockEE2Size && arpPattern.ExtendedException[i].ReservedBlockEE2Size < _MaxReservedBlock)
               {
                  Parser.GetBYTES(arpPattern.ExtendedException[i].ReservedBlockEE2Size,&arpPattern.ExtendedException[i].ReservedBlockEE2);
               }
            }
         }
      }
   }
   Parser.GetDWORD(&arpPattern.ReservedBlock2Size);
   if (arpPattern.ReservedBlock2Size && arpPattern.ReservedBlock2Size < _MaxReservedBlock)
   {
      Parser.GetBYTES(arpPattern.ReservedBlock2Size,&arpPattern.ReservedBlock2);
   }
   // Junk data remains.
   if (Parser.RemainingBytes() > 0)
   {
      arpPattern.JunkDataSize = Parser.RemainingBytes();
      Parser.GetBYTES(arpPattern.JunkDataSize,&arpPattern.JunkData);
   }
   AppointmentRecurrencePatternStruct* parpPattern = new AppointmentRecurrencePatternStruct;
   if (parpPattern)
   {
      *parpPattern = arpPattern;
   }
   return parpPattern;
}

```

## <a name="see-also"></a>Consulte también

- [Uso de MAPI para crear elementos de Outlook 2007](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

