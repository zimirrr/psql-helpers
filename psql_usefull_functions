CREATE OR REPLACE FUNCTION stringInt_to_integer(v_input text) RETURNS INTEGER AS $$
DECLARE 
    v_int_value INTEGER DEFAULT 0;
BEGIN
    BEGIN
        IF v_input IS NULL THEN
            v_int_value := 0;
        ELSE
            v_int_value := v_input::INTEGER;
        END IF;
    EXCEPTION WHEN OTHERS THEN
        RAISE NOTICE 'Invalid integer value: "%".  Returning 0.', v_input;
        RETURN 0;
    END;
RETURN v_int_value;
END;
$$ LANGUAGE plpgsql;
